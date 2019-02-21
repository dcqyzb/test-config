# test-config
配置中心-测试

# 配置中心放置配置文件格式为：
     http请求地址和资源文件映射如下:
              /{application}/{profile}[/{label}]
              /{application}-{profile}.yml
              /{label}/{application}-{profile}.yml
              /{application}-{profile}.properties
              /{label}/{application}-{profile}.properties
              
           application:项目名
           profile:dev开发环境配置文件、test测试环境、pro正式环境
           lable:远程创库分支
           
# spring cloud 配置中心服务配置：
‘```yml
spring:
  application:
    name: config-server
  cloud:
    config:
      server:
        git:
          uri: https://github.com/dcqyzb/test-config.git #配置git仓库地址
          search-paths: dctestConfig  #配置仓库路径
          username: git用户名
          password: git密码
      label: master
```’
