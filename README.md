**项目文档生成工具**
    


* 修改gradle.build文件

        ext {
            swaggerVersion = "v2"
            swaggerPath = "api-docs"
            
            //修改以下配置
            apiLocatoin = "http://10.52.2.170:7002"     //接口地址
            apiGroup = "内部接口"                        //接口分组名
        }


* 执行gradle clean asciidoctor命令生成文档

* 文件说明：

        build
            asciidoc
                generated
                    definitions.adoc    //数据结构定义
                    overview.adoc       //概述
                    paths.adoc          //API文档
                    security.adoc       
                html5                   //最终生成文档
                    index.html
            swagger
                swagger.json            //临时文件
        src
            docs
                asciidoc
                    extensions          //扩展点
                    appendices.adoc     //文档附加数据
                    demo.adoc           //Demo
                    index.adoc          //主文档
                    manual.adoc         //操作手册
                    records.adoc        //文档修改记录
                    records-demo.adoc   //文档修改记录Demo