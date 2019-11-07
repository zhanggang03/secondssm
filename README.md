四个包：pojo,service,dao,controller，其所存放的分别是：

pojo: 存放自定义的java类。如：paper类，user类，book类等，每个类的属性设为private，并提供public属性的getter/setter方法让外界访问
service：定义接口，包含系统所提供的功能。（之后还会在service包下再新建impl包）。
dao：定义接口，包含与数据库进行交互的功能。
controller：控制器，负责接收页面请求，转发和处理。


在resource包下新建Directory：“mapper”（用于存放xxxMapper.xml文件）和“spring”
（用于存放spring-xxx.xml配置文件），新建文件：“jdbc.properties”（mysql数据库配置文件）,
”log4j.properties”（日志输出配置文件）,”mybatis-config.xml”（mybatis框架配置文件）。 

数据库初始化：
SET FOREIGN_KEY_CHECKS=0;
 
-- ----------------------------
-- Table structure for `paper`
-- ----------------------------
DROP TABLE IF EXISTS `paper`;
CREATE TABLE `paper` (
  `paper_id` bigint(20) NOT NULL AUTO_INCREMENT COMMENT 'paperID',
  `name` varchar(100) NOT NULL COMMENT 'paper名称',
  `number` int(11) NOT NULL COMMENT 'paper数量',
  `detail` varchar(200) NOT NULL COMMENT 'paper描述',
  PRIMARY KEY (`paper_id`)
) ENGINE=InnoDB AUTO_INCREMENT=12 DEFAULT CHARSET=utf8 COMMENT='paper表';
 
-- ----------------------------
-- Records of paper
-- ----------------------------
INSERT INTO `paper` VALUES ('1', '机器学习', '2', 'mlmlmlml');
INSERT INTO `paper` VALUES ('2', '深度学习', '3', 'dldldl');
INSERT INTO `paper` VALUES ('3', '大数据', '4', 'bdbdbd');