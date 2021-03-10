## 极客时间课后作业

### 第二周

##### 作业运行说明

```shell
mvn clean package -U
java -jar .\user-web\target\user-web-v1-SNAPSHOT-war-exec.jar
```

运行成功后，可访问 http://localhost:8080/register-form 注册用户

注册成功后跳转至登录页 http://localhost:8080/login-form 进行登录

查询所有用户 http://localhost:8080/user 返回用户Json数据

登录成功会forward到登录成功的提示页，在提示页可查询所有的用户，以Json形式返回用户数据，若用户名或密码错误则forward到错误提示页。

内部使用JNDI上下文实现依赖注入，使用hibernate validator校验手机/密码，若字段不符合校验要求则会返回校验错误信息Json数据，提示字段与对应的错误信息。