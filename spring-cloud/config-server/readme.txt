注意事项：
· 配置文件默认以dev结尾，如abc-dev.properties，像config1.properties, config-demo.yml等文件是读取不到的。
  若需要修改，则添加配置：spring.cloud.config.profile=dev
· spring.cloud.config.server.git.uri一定要是仓库跟目录，否则会报错：can not clone root Repository
  一般可能会单独拿个仓库来装配置文件
· url访问方式：
	http://localhost:8082/config1/dev			√ config1 文件名
	http://localhost:8082/fieldp/dev			√ fieldp config1里的属性名
	http://localhost:8082/config1/fieldp/dev	× 