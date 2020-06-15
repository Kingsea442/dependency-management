# 基础依赖管理

构建：gradle local 可以将包发布到本地仓库中

使用方式比如：
```
buildscript {
    dependencies {
        classpath "io.spring.gradle:dependency-management-plugin:$dependencyManagementVersion"
    }
}

apply plugin: "io.spring.dependency-management"
dependencyManagement {
    imports {
        mavenBom "com.sea:dependency-management:1.0-SNAPSHOT"
    }
}

dependencies {
    implementation "org.slf4j:slf4j-api"
    implementation "org.apache.commons:commons-collections4"
    implementation "com.google.guava:guava"
}
```