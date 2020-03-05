# 快速启动

我们为您提供了在线版的代码生成器，您可以打开以下网址进行使用。

https://builder.faster.xiaoguikeji.cn/

> 在线版仅支持生成Faster-Framework最新版本的的代码。

> 如果您需要生成旧版本，可以访问[github](https://github.com/faster-framework/faster-framework-builder/releases)下载每个版本的代码生成器，本地运行，具体方法将在[进阶](/advanced/deploy/)中介绍。

接下来我们将为您介绍如何使用代码生成器。

## 数据库创建

首先，我们需要创建数据库及表，提供一个示例：

```
CREATE DATABASE faster_api_test;

USE faster_api_test;
 
CREATE TABLE `tb_video` (
  `id` bigint(20) NOT NULL,
  `name` varchar(128) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '标题',
  `url` varchar(1024) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT 'url地址',
  `img` varchar(1024) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '封面图片',
  `content` longtext CHARACTER SET utf8mb4 COLLATE utf8mb4_bin COMMENT '内容',
  `time` int(11) DEFAULT NULL COMMENT '时长',
  `create_by` bigint(20) DEFAULT NULL COMMENT '创建人',
  `update_by` bigint(20) DEFAULT NULL COMMENT '最后更新人',
  `create_date` datetime NOT NULL COMMENT '创建时间',
  `update_date` datetime NOT NULL COMMENT '最后更新时间',
  `sort` int(11) NOT NULL DEFAULT '0' COMMENT '排序',
  `remark` varchar(1024) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '备注',
  `deleted` tinyint(4) NOT NULL DEFAULT '0' COMMENT '是否删除（0.,否 1.是）'
  PRIMARY KEY (`id`) USING BTREE,
  KEY `idx_category_id` (`category_id`) USING BTREE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='视频表';
```

> 如果要使用代码生成器，那么我们的表中必须包含create_by、update_by、create_date、update_date、sort、remark、deleted这些公共字段。

## 项目下载

在代码生成器中，选择我们希望生成的项目，填写数据库相关信息，点击下载项目，即可获取压缩包。

## 项目导入与运行

- 接口、后台管理接口、后台管理接口合并项目需要使用java、maven环境，我们需要使用IDEA进行导入，具体可以参见[此处](https://admin.faster.org.cn/#/intro/quickstart/run-api)。
- 后台管理前端需要使用Node环境，具体可以参见[此处](https://admin.faster.org.cn/#/intro/quickstart/run-web)。