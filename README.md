# 前言

欢迎来到果蔬作物疾病防治系统项目，本项目是一款基于Java开发的实用性农业辅助系统。通过此项目，希望为广大农业生产者提供一套便捷、高效的农作物疾病防治方案。以下为项目的详细介绍。

## 内容介绍

果蔬作物疾病防治系统旨在帮助农户及时识别和处理果蔬作物生长过程中的各种疾病。系统主要包括以下功能：用户注册登录、作物信息管理、疾病知识库、在线咨询、防治方案推荐等。用户可以根据自己的需求在系统中查询疾病信息、学习防治知识，并获得针对性的防治建议，从而提高农业生产效益。

## 技术介绍

本项目采用以下技术栈进行开发：

- **语言：Java**
- **使用框架：Spring Boot**
- **前端技术：JS、Vue、css3**
- **开发工具：IDEA/Eclipse**
- **数据库：MySQL 5.7/8.0**
- **数据库管理工具：phpstudy/Navicat**
- **JDK版本：jdk1.8**
- **Maven: apache-maven 3.8.1-bin**
- **前端环境：Node.Js 12\14\16**

## 核心代码

以下为项目中的一部分核心代码，展示了如何实现疾病防治方案推荐功能：

```java
// DiseaseController.java
@GetMapping("/recommend")
public ResponseEntity recommend(@RequestParam("cropId") Integer cropId, @RequestParam("diseaseId") Integer diseaseId) {
    Disease disease = diseaseService.findById(diseaseId);
    Crop crop = cropService.findById(cropId);
    if (disease == null || crop == null) {
        return ResponseEntity.badRequest().body("Invalid parameters.");
    }
    List<PreventionScheme> schemes = preventionSchemeService.findByDiseaseId(diseaseId);
    // Filter schemes based on crop type
    schemes = schemes.stream().filter(scheme -> scheme.getCropType().equals(crop.getType())).collect(Collectors.toList());
    return ResponseEntity.ok(schemes);
}
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图

![封面图片](https://img11.360buyimg.com/ddimg/jfs/t1/320897/18/25475/197420/689e9c0aF4ba8fb59/2a09390ce1b7e0e3.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/312358/9/26646/138493/689e9be8Fb3e60e95/320e91e81b3188c6.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/309996/29/26671/141692/689e9be9Fb3cc81a9/e7c3a183bf8bf323.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/311096/14/26712/29220/689e9beaF8dc9f04e/f524cd7574e668d4.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/327967/23/4651/36129/689e9beaF0c7ddaa0/fe02fd8a4e8c600b.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/320602/27/24889/35490/689e9bebFbdb645ae/aa81198f5cee53ce.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/291562/27/19038/93777/689e9becFdd834581/ad788c6b8ef8a4c1.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/316185/7/26555/38040/689e9bedFc6cd86ec/a4f3231305bcaa80.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/324462/5/4742/32958/689e9beeF9546f3e4/48880d242f9afbff.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/311720/30/26712/42767/689e9befF2db6b5b3/e6122ca2cb3656cb.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
