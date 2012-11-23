---
layout: post
title: 获取数码照片的metadata信息
description: ""
category: tech
tags: [groovy java]
published: true
---

最近买了台单反相机，因此对拍出来的图片的详细信息（如：ISO，光圈大小，焦距等）特别感兴趣，因此尝试看是否能写个程序一次性的读取。

实现程序主要使用 [metadata-extractor](http://code.google.com/p/metadata-extractor/) 库，并且使用groovy来实现

具体代码如下:

    import javax.imageio.ImageIO
    import com.drew.imaging.jpeg.JpegMetadataReader
    import com.drew.metadata.Directory
    import com.drew.metadata.Metadata
    import com.drew.metadata.Tag
    import com.drew.metadata.exif.ExifIFD0Directory
    import com.drew.metadata.exif.ExifSubIFDDirectory
    
    //打算直接读取网络图片文件，但还没有测试成功
    //def url = new URL("http://metadata-extractor.googlecode.com/git/Tests/com/drew/metadata/exif/nikonMakernoteType2b.jpg")
    //ByteArrayOutputStream baos = new ByteArrayOutputStream();
    //ImageIO.write(ImageIO.read(url), "png", baos);
    //InputStream is = new ByteArrayInputStream(baos.toByteArray());
    //Metadata metadata = JpegMetadataReader.readMetadata(is,true);
    
    def jpegFile = new File("resource/nikonMakernoteType2b.jpg");//注意，网上找的很多图片文件并没有exif信息，应该是上传被存储时丢失了
    Metadata metadata = JpegMetadataReader.readMetadata(jpegFile);
    Directory exif = metadata.getDirectory(ExifIFD0Directory.class);
    Directory exifSub = metadata.getDirectory(ExifSubIFDDirectory.class);
    exif?.tags.each { tag ->
        println "[$tag.tagName] $tag.description"
    }
    exifSub?.tags.each { tag ->
        println "[$tag.tagName] $tag.description"
    }