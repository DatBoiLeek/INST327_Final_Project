CREATE DATABASE  IF NOT EXISTS `team_project` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci */ /*!80016 DEFAULT ENCRYPTION='N' */;
USE `team_project`;
-- MySQL dump 10.13  Distrib 8.0.28, for Win64 (x86_64)
--
-- Host: 127.0.0.1    Database: team_project
-- ------------------------------------------------------
-- Server version	8.0.28

/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!50503 SET NAMES utf8 */;
/*!40103 SET @OLD_TIME_ZONE=@@TIME_ZONE */;
/*!40103 SET TIME_ZONE='+00:00' */;
/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

--
-- Table structure for table `console_platform`
--

DROP TABLE IF EXISTS `console_platform`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `console_platform` (
  `console_platform_id` int NOT NULL,
  `game_platforms` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`console_platform_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `console_platform`
--

LOCK TABLES `console_platform` WRITE;
/*!40000 ALTER TABLE `console_platform` DISABLE KEYS */;
INSERT INTO `console_platform` VALUES (1,'PS4'),(2,'XBOX ONE'),(3,'SWITCH'),(4,'XBOX 360'),(5,'WII'),(6,'SNES'),(7,'PS1'),(8,'PS2'),(9,'XBOX'),(10,'PSP'),(11,'NINTENDO 3DS'),(12,'GAMECUBE'),(13,'SEGA GENESIS'),(14,'PS5'),(15,'NINTENDO 64'),(16,'PS3'),(17,'PC');
/*!40000 ALTER TABLE `console_platform` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Temporary view structure for view `count_game_sales`
--

DROP TABLE IF EXISTS `count_game_sales`;
/*!50001 DROP VIEW IF EXISTS `count_game_sales`*/;
SET @saved_cs_client     = @@character_set_client;
/*!50503 SET character_set_client = utf8mb4 */;
/*!50001 CREATE VIEW `count_game_sales` AS SELECT 
 1 AS `game_id`,
 1 AS `count`*/;
SET character_set_client = @saved_cs_client;

--
-- Table structure for table `customer`
--

DROP TABLE IF EXISTS `customer`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `customer` (
  `customer_id` int NOT NULL,
  `c_first_name` varchar(40) NOT NULL,
  `c_last_name` varchar(40) NOT NULL,
  `phone_number` varchar(50) NOT NULL,
  `customer_address_1` varchar(50) NOT NULL,
  `customer_address_2` varchar(50) DEFAULT NULL,
  `customer_city` varchar(50) NOT NULL,
  `customer_state` char(2) DEFAULT NULL,
  `customer_zip_code` varchar(50) NOT NULL,
  PRIMARY KEY (`customer_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `customer`
--

LOCK TABLES `customer` WRITE;
/*!40000 ALTER TABLE `customer` DISABLE KEYS */;
INSERT INTO `customer` VALUES (0,'Kennen','Linette','(861) 186-7921','2654 Quiet Water Cove',NULL,'Annapolis','MA','21401'),(1,'Siana','Shanahan','(725) 364-4494','864 Main Street',NULL,'Worcester','AL','1610'),(2,'Danyle','Sitarski','(728) 154-7870','4216 Park Boulevard',NULL,'Montgomery','AK','36106'),(3,'Jacquelyn','Fayola','(629) 952-4526','4800 Huffman Road',NULL,'Anchorage','MA','99516'),(4,'Lakin','Cyrus','(165) 847-0549','9 Pierce Road',NULL,'Watertown','DC','2472'),(5,'Lakeia','Alpert','(271) 154-3747','3553 Brandywine Street Northwest',NULL,'Washington','AL','20008'),(6,'Jonathen','Cann','(321) 518-5242','713 Millard Fuller Drive',NULL,'Montgomery','CA','36110'),(7,'Landry','Rattan','(631) 261-0222','1061 Sumatra Street',NULL,'Hayward','DC','94544'),(8,'Joely','Cryan','(431) 641-3863','3500 Blanchard Drive Southwest',NULL,'Washington','AZ','20032'),(9,'Amonda','Gertrud','(854) 854-9888','130 West Brown Road',NULL,'Mesa','KY','85201'),(10,'Bernadette','Cosenza','(228) 722-8798','1014 South 2nd Street',NULL,'Louisville','AR','40203'),(11,'Kandus','Cole','(397) 755-3334','325 Baxter Lane',NULL,'Fayetteville','DC','72701'),(12,'Norvell','Billi','(487) 355-3837','643 Farragut Street Northwest',NULL,'Washington','AR','20011'),(13,'Wray','Payton','(258) 151-4437','1828 East Parkshore Drive',NULL,'Fayetteville','FL','72703'),(14,'Jonahtan','Yetah','(513) 373-6816','1906 Palmetto Avenue',NULL,'Panama City','MA','32405'),(15,'Dontavious','Rachelle','(643) 743-8634','17 Elm Street',NULL,'Cambridge','CT','2139'),(16,'Jillienne','Vudimir','(318) 383-8046','199 Spencer Street',NULL,'Manchester','MA','6040'),(17,'Casidy','Wilmer','(865) 558-3842','2375 Main Street',NULL,'Palmer','TN','1069'),(18,'Eliott','Toomay','(103) 138-4945','2205 Lindell Avenue',NULL,'Nashville','TN','37204'),(19,'Emilio','Clein','(919) 548-7315','1267 Martin Street',NULL,'Nashville','AL','37203'),(20,'Elice','Manly','(919) 393-7790','1217 Cottondale Road',NULL,'Montgomery','CO','36109'),(21,'Annelies','Mond','(985) 825-8244','1169 East Hopkins Avenue',NULL,'Aspen','VT','81611'),(22,'Kalea','Dorene','(720) 527-5281','536 Walters Farm Road',NULL,'East Haven','AL','5837'),(23,'Derwin','Grania','(730) 551-6333','788 Williamson Road',NULL,'Montgomery','DC','36109'),(24,'Nydia','Cadmar','(640) 656-3788','1707 6th Street Northwest',NULL,'Washington','AL','20001'),(25,'Judah','Cherice','(127) 531-8204','1163 Rosedale Drive',NULL,'Montgomery','AR','36107'),(26,'Jumaane','Wollis','(796) 906-8401','600 West North Street',NULL,'Fayetteville','MD','72701'),(27,'Rayshaun','Ulises','(870) 834-2315','7802 Titan Court',NULL,'Pasadena','MA','21122'),(28,'Bud','Fabian','(934) 869-9144','8 Chestnut Street',NULL,'Winchester','FL','1890'),(29,'Becky','Lotus','(623) 650-4926','8221 Surf Drive',NULL,'Panama City','MA','32408'),(30,'Ariele','Valiant','(916) 331-3614','61 Thomas Street',NULL,'Dedham','CA','2026'),(31,'Tyffanie','Calondra','(680) 721-8402','1139 Addison Street',NULL,'Berkeley','CT','94702'),(32,'Shaunette','Hubert','(171) 744-4842','14 Linden Street',NULL,'Manchester','MA','6040'),(33,'Cinthia','Fulmis','(659) 158-6423','2A Cleveland Park Rd',NULL,'Freetown','CA','2717'),(34,'Deleon','Rurik','(758) 324-8076','31 Yosemite Avenue',NULL,'Oakland','CT','94611'),(35,'Sydnie','Blank','(758) 324-8076','39 Tania Drive',NULL,'Manchester','AZ','6040'),(36,'Aakash','Furt','(659) 155-6424','6060 West Royal Palm Road',NULL,'Glendale','AK','85302');
/*!40000 ALTER TABLE `customer` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Temporary view structure for view `customer_more_than_one`
--

DROP TABLE IF EXISTS `customer_more_than_one`;
/*!50001 DROP VIEW IF EXISTS `customer_more_than_one`*/;
SET @saved_cs_client     = @@character_set_client;
/*!50503 SET character_set_client = utf8mb4 */;
/*!50001 CREATE VIEW `customer_more_than_one` AS SELECT 
 1 AS `customer`,
 1 AS `quantity`,
 1 AS `item_total`*/;
SET character_set_client = @saved_cs_client;

--
-- Table structure for table `customer_order`
--

DROP TABLE IF EXISTS `customer_order`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `customer_order` (
  `purchase_id` int NOT NULL,
  `purchase_date` date NOT NULL,
  `game_id` int DEFAULT NULL,
  `customer_id` int DEFAULT NULL,
  PRIMARY KEY (`purchase_id`),
  KEY `game_id` (`game_id`),
  KEY `customer_id` (`customer_id`),
  CONSTRAINT `customer_id` FOREIGN KEY (`customer_id`) REFERENCES `customer` (`customer_id`),
  CONSTRAINT `game_id` FOREIGN KEY (`game_id`) REFERENCES `game` (`game_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `customer_order`
--

LOCK TABLES `customer_order` WRITE;
/*!40000 ALTER TABLE `customer_order` DISABLE KEYS */;
INSERT INTO `customer_order` VALUES (1,'2022-01-05',1,0),(2,'2022-01-07',3,4),(3,'2022-01-14',2,9),(4,'2022-01-19',7,13),(5,'2022-01-25',21,2),(6,'2022-02-01',20,8),(7,'2022-02-04',24,18),(8,'2022-02-06',27,22),(9,'2022-02-10',33,10),(10,'2022-02-11',29,1),(11,'2022-02-15',30,5),(12,'2022-02-17',25,6),(13,'2022-02-20',28,29),(14,'2022-02-21',32,12),(15,'2022-02-21',31,19),(16,'2022-02-24',34,17),(17,'2022-02-25',6,21),(18,'2022-02-28',18,23),(19,'2022-03-01',8,25),(20,'2022-03-02',4,16),(21,'2022-03-05',5,7),(22,'2022-03-06',17,3),(23,'2022-03-07',12,11),(24,'2022-03-07',10,14),(25,'2022-03-09',23,20),(26,'2022-03-10',14,15),(27,'2022-03-13',9,26),(28,'2022-03-17',19,24),(29,'2022-03-20',15,27),(30,'2022-03-25',11,28),(31,'2022-03-26',16,30),(32,'2022-03-30',35,31),(33,'2022-04-02',22,35),(34,'2022-04-03',36,32),(35,'2022-04-06',26,34),(36,'2022-04-07',3,32),(37,'2022-04-10',6,36),(38,'2022-04-12',30,33);
/*!40000 ALTER TABLE `customer_order` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Temporary view structure for view `customer_order_count`
--

DROP TABLE IF EXISTS `customer_order_count`;
/*!50001 DROP VIEW IF EXISTS `customer_order_count`*/;
SET @saved_cs_client     = @@character_set_client;
/*!50503 SET character_set_client = utf8mb4 */;
/*!50001 CREATE VIEW `customer_order_count` AS SELECT 
 1 AS `customer`,
 1 AS `customer_phone_number`,
 1 AS `quantity`,
 1 AS `game_title`,
 1 AS `esrb_rating`,
 1 AS `publisher_name`,
 1 AS `confirmation_number`,
 1 AS `shipped_date`,
 1 AS `item_total`*/;
SET character_set_client = @saved_cs_client;

--
-- Table structure for table `employee`
--

DROP TABLE IF EXISTS `employee`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `employee` (
  `emp_id` int NOT NULL,
  `first_name` varchar(40) NOT NULL,
  `last_name` varchar(40) NOT NULL,
  `retailer_id_1` int DEFAULT NULL,
  PRIMARY KEY (`emp_id`),
  KEY `retailer_id_1` (`retailer_id_1`),
  CONSTRAINT `retailer_id_1` FOREIGN KEY (`retailer_id_1`) REFERENCES `game_retailers` (`retailer_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `employee`
--

LOCK TABLES `employee` WRITE;
/*!40000 ALTER TABLE `employee` DISABLE KEYS */;
INSERT INTO `employee` VALUES (0,'Tracy','Roberts',1),(1,'Marie','Mason',2),(2,'Michelle','Wise',3),(3,'Gordon','Owens',4),(4,'Mason','Mills',5),(5,'Monique','Sullivan',6),(6,'Sarah','Ramirez',7),(7,'Gina','Schroeder',8),(8,'Kevin','Garza',9),(9,'Amanda','Baker',10),(10,'Richard','Adams',11),(11,'Derek','Obrien',12),(12,'Angel','Murphy',13),(13,'Mindy','Cox',14),(14,'Cynthia','King',15),(15,'Matthew','Odonnell',16),(16,'Melanie','Walsh',17);
/*!40000 ALTER TABLE `employee` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `game`
--

DROP TABLE IF EXISTS `game`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `game` (
  `game_id` int NOT NULL,
  `game_title` varchar(100) DEFAULT NULL,
  `price` decimal(4,2) NOT NULL,
  `esrb_rating` varchar(40) DEFAULT NULL,
  `publisher_id` int DEFAULT NULL,
  `genre_id` int DEFAULT NULL,
  `retailer_id` int DEFAULT NULL,
  `console_id` int DEFAULT NULL,
  PRIMARY KEY (`game_id`),
  KEY `publisher_id` (`publisher_id`),
  KEY `genre_id` (`genre_id`),
  KEY `retailer_id` (`retailer_id`),
  KEY `console_id` (`console_id`),
  CONSTRAINT `console_id` FOREIGN KEY (`console_id`) REFERENCES `console_platform` (`console_platform_id`),
  CONSTRAINT `genre_id` FOREIGN KEY (`genre_id`) REFERENCES `genre` (`genre_id`),
  CONSTRAINT `publisher_id` FOREIGN KEY (`publisher_id`) REFERENCES `publisher` (`publisher_id`),
  CONSTRAINT `retailer_id` FOREIGN KEY (`retailer_id`) REFERENCES `game_retailers` (`retailer_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `game`
--

LOCK TABLES `game` WRITE;
/*!40000 ALTER TABLE `game` DISABLE KEYS */;
INSERT INTO `game` VALUES (1,'Battle of Heroes 3',2.99,'E',1,11,11,17),(2,'Grand Theft Auto 5',22.78,'M',2,10,17,16),(3,'VA-11 Hall-A',14.99,'M',3,15,11,17),(4,'Mario Kart 8 Deluxe',59.99,'E',4,5,7,3),(5,'Super Mario Party',59.99,'E',4,16,7,3),(6,'Super Smash Bros. Ultimate',59.99,'E',4,16,7,3),(7,'Halo Reach',59.99,'M',5,6,10,4),(8,'Marvel Spiderman',59.99,'T',6,1,1,1),(9,'Resident Evil 5',26.00,'M',7,2,10,16),(10,'Kingdom Hearts 1.5 HD Remix',9.99,'T',8,1,9,16),(11,'Rayman Origins',19.99,'E',9,4,11,17),(12,'Space Channel 5',39.99,'E',10,13,17,8),(13,'Gears of War Trilogy',24.95,'M',11,6,14,2),(14,'Max Payne 2',14.99,'M',2,6,11,2),(15,'Darksiders 2',29.99,'M',12,1,11,17),(16,'7 Days to Die',29.99,'M',13,2,17,1),(17,'Metroid Dread',59.99,'E',4,5,7,3),(18,'Call of Duty: Black Ops II',59.99,'M',14,6,11,17),(19,'Elden Ring',59.99,'M',15,2,1,2),(20,'The Incredible Hulk: Ultimate Destruction',18.51,'T',16,1,6,12),(21,'The Legend of Zelda: Ocarina of Time 3D',24.00,'E',4,4,7,11),(22,'Teenage Mutant Ninja Turtles: The Cowabunga Collection',39.99,'T',17,12,3,14),(23,'EarthBound',34.90,'T',4,16,4,6),(24,'God of War: Chains of Olympus',29.99,'M',18,1,14,10),(25,'Spiderman 2: Enter Electro',30.22,'T',14,1,16,7),(26,'Def Jam Vendetta',30.00,'T',19,8,17,8),(27,'Super Mario Galaxy',28.99,'E',4,4,7,5),(28,'Record of Lodoss War: Deedlit In Wonder Labyrinth',29.99,'T',20,16,12,1),(29,'Banjo-Kazooie',28.99,'E',4,4,17,15),(30,'Demon Turf',24.99,'E',21,4,11,17),(31,'Risk of Rain 2',24.99,'T',22,6,11,17),(32,'Resident Evil 4',19.99,'M',7,2,14,8),(33,'Forza Horizon 5',45.99,'E',11,5,9,2),(34,'Deus Ex',6.99,'M',8,7,11,17),(35,'Grand Theft Auto 5',20.36,'M',2,10,17,4),(36,'Kingdom Hearts 1.5 + 2.5 Remix',10.99,'E',8,1,9,1);
/*!40000 ALTER TABLE `game` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `game_retailers`
--

DROP TABLE IF EXISTS `game_retailers`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `game_retailers` (
  `retailer_id` int NOT NULL,
  `retailer_name` varchar(40) NOT NULL,
  `retailer_phone_number` varchar(50) DEFAULT NULL,
  `retailer_address_1` varchar(50) DEFAULT NULL,
  `retailer_address_2` varchar(50) DEFAULT NULL,
  `retailer_city` varchar(50) DEFAULT NULL,
  `retailer_state` char(2) DEFAULT NULL,
  `retailer_zip_code` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`retailer_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `game_retailers`
--

LOCK TABLES `game_retailers` WRITE;
/*!40000 ALTER TABLE `game_retailers` DISABLE KEYS */;
INSERT INTO `game_retailers` VALUES (1,'GameStop','(703) 578-9449','3519 S Jefferson St',NULL,'Baileys Crossroads','VA','22041'),(2,'Best Buy','(202) 387-6150','3100 14th St','NW Ste 203','Washington','DC','20010'),(3,'Target','(301) 645-7114','3300 Western Pkwy',NULL,'Waldorf','MD','20603'),(4,'RetroGamingStores','(323) 617-3657','848 N','Rainbow Blvd','Las Vegas','NV','89107'),(5,'EB Games','(252) 492-5269','390 N Cooper Dr',NULL,'Henderson','NC','27536'),(6,'Electronics Flip','(440) 459-1630','5280 Mayfield Rd ',NULL,'Lyndhurst','OH','44124'),(7,'Nintendo NY','(646) 459-0800','10 Rockefeller Plaza','Floor 1','New York','NY','10020'),(8,'Records & Rarities','(703) 313-0100','6500 Springfield Mall',NULL,'Springfield','VA','22150'),(9,'GameStop','(301) 599-0346','8871 Branch Ave #10',NULL,'Clinton','MD','20735'),(10,'Amazon','(206) 508-4051',NULL,NULL,NULL,NULL,NULL),(11,'Steam','(425) 889-9642',NULL,NULL,NULL,NULL,NULL),(12,'J & L','(212) 233-3399','1026 6th Ave','Floor 1','New York','NY','10018'),(13,'Target','(715) 341-8790','5300 US-10 E',NULL,'Stevens Point','WI','54482'),(14,'Walmart','(719) 578-9164','3201 E Platte Ave',NULL,'Colorado Springs','CO','80909'),(15,'G2A','(852) 580-85226',NULL,NULL,NULL,NULL,NULL),(16,'eStarland','(866) 703-0866','14225 Sullyfield Cir','Suite C','Chantilly','VA','20151'),(17,'eBay','(866) 961-9253',NULL,NULL,NULL,NULL,NULL);
/*!40000 ALTER TABLE `game_retailers` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Temporary view structure for view `games_below_40`
--

DROP TABLE IF EXISTS `games_below_40`;
/*!50001 DROP VIEW IF EXISTS `games_below_40`*/;
SET @saved_cs_client     = @@character_set_client;
/*!50503 SET character_set_client = utf8mb4 */;
/*!50001 CREATE VIEW `games_below_40` AS SELECT 
 1 AS `game_title`,
 1 AS `price`*/;
SET character_set_client = @saved_cs_client;

--
-- Table structure for table `genre`
--

DROP TABLE IF EXISTS `genre`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `genre` (
  `genre_id` int NOT NULL,
  `genre_name` varchar(40) NOT NULL,
  PRIMARY KEY (`genre_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `genre`
--

LOCK TABLES `genre` WRITE;
/*!40000 ALTER TABLE `genre` DISABLE KEYS */;
INSERT INTO `genre` VALUES (1,'Action-Adventure'),(2,'Survival Horror'),(3,'Puzzle'),(4,'Platform'),(5,'Racing'),(6,'Shooter'),(7,'Simulation'),(8,'Sports'),(9,'Strategy'),(10,'Sandbox'),(11,'MOBA'),(12,'Fighting'),(13,'Rhythm'),(14,'Metroidvania'),(15,'Visual Novel'),(16,'RPG');
/*!40000 ALTER TABLE `genre` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `order_carrier`
--

DROP TABLE IF EXISTS `order_carrier`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `order_carrier` (
  `order_carrier_id` int NOT NULL,
  `order_carrier_name` varchar(50) NOT NULL,
  PRIMARY KEY (`order_carrier_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `order_carrier`
--

LOCK TABLES `order_carrier` WRITE;
/*!40000 ALTER TABLE `order_carrier` DISABLE KEYS */;
INSERT INTO `order_carrier` VALUES (1,'FedEx'),(2,'UPS'),(3,'Amazon'),(4,'DHL'),(5,'USPS');
/*!40000 ALTER TABLE `order_carrier` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Table structure for table `publisher`
--

DROP TABLE IF EXISTS `publisher`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `publisher` (
  `publisher_id` int NOT NULL,
  `publisher_name` varchar(50) NOT NULL,
  PRIMARY KEY (`publisher_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `publisher`
--

LOCK TABLES `publisher` WRITE;
/*!40000 ALTER TABLE `publisher` DISABLE KEYS */;
INSERT INTO `publisher` VALUES (1,'Astafiev Egor'),(2,'Rockstar Games'),(3,'Ysbryd Games'),(4,'Nintendo'),(5,'Bungie'),(6,'Insomniac'),(7,'Capcom'),(8,'Square-Enix'),(9,'Ubisoft'),(10,'Sega'),(11,'Microsoft'),(12,'THQ Nordic'),(13,'Telltale Games '),(14,'Activision '),(15,'Bandai Namco Entertainment'),(16,'Vivendi Games'),(17,'Konami'),(18,'Sony'),(19,'Electronic Arts'),(20,'Red Art Games'),(21,'Playtonic Friends'),(22,'Hopoo Games');
/*!40000 ALTER TABLE `publisher` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Temporary view structure for view `publisher_and_retailer_info`
--

DROP TABLE IF EXISTS `publisher_and_retailer_info`;
/*!50001 DROP VIEW IF EXISTS `publisher_and_retailer_info`*/;
SET @saved_cs_client     = @@character_set_client;
/*!50503 SET character_set_client = utf8mb4 */;
/*!50001 CREATE VIEW `publisher_and_retailer_info` AS SELECT 
 1 AS `game_title`,
 1 AS `game_platforms`,
 1 AS `publisher_name`,
 1 AS `retailer_name`,
 1 AS `retailer city/state`,
 1 AS `employee`,
 1 AS `retailer_phone_number`*/;
SET character_set_client = @saved_cs_client;

--
-- Table structure for table `shipping`
--

DROP TABLE IF EXISTS `shipping`;
/*!40101 SET @saved_cs_client     = @@character_set_client */;
/*!50503 SET character_set_client = utf8mb4 */;
CREATE TABLE `shipping` (
  `confirmation_number` int NOT NULL,
  `customer_id_ship` int DEFAULT NULL,
  `game_id_ship` int DEFAULT NULL,
  `emp_id_ship` int DEFAULT NULL,
  `shipped_date` date NOT NULL,
  `order_carrier_id` int DEFAULT NULL,
  PRIMARY KEY (`confirmation_number`),
  KEY `order_carrier_id` (`order_carrier_id`),
  KEY `game_id_ship` (`game_id_ship`),
  KEY `customer_id_ship` (`customer_id_ship`),
  KEY `emp_id_ship` (`emp_id_ship`),
  CONSTRAINT `customer_id_ship` FOREIGN KEY (`customer_id_ship`) REFERENCES `customer` (`customer_id`),
  CONSTRAINT `emp_id_ship` FOREIGN KEY (`emp_id_ship`) REFERENCES `game_retailers` (`retailer_id`),
  CONSTRAINT `game_id_ship` FOREIGN KEY (`game_id_ship`) REFERENCES `game` (`game_id`),
  CONSTRAINT `order_carrier_id` FOREIGN KEY (`order_carrier_id`) REFERENCES `order_carrier` (`order_carrier_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
/*!40101 SET character_set_client = @saved_cs_client */;

--
-- Dumping data for table `shipping`
--

LOCK TABLES `shipping` WRITE;
/*!40000 ALTER TABLE `shipping` DISABLE KEYS */;
INSERT INTO `shipping` VALUES (1,0,1,9,'2022-01-05',1),(2,4,3,3,'2022-01-07',2),(3,9,2,14,'2022-01-14',1),(4,13,7,7,'2022-01-19',1),(5,2,21,10,'2022-01-25',2),(6,8,20,6,'2022-02-01',3),(7,18,24,11,'2022-02-04',4),(8,22,27,12,'2022-02-06',5),(9,10,33,15,'2022-02-10',1),(10,1,29,1,'2022-02-11',2),(11,5,30,2,'2022-02-15',5),(12,6,25,8,'2022-02-17',3),(13,29,28,13,'2022-02-20',4),(14,12,32,4,'2022-02-21',1),(15,19,31,5,'2022-02-21',2),(16,17,34,16,'2022-02-24',3),(17,21,6,7,'2022-02-25',3),(18,23,18,8,'2022-02-28',4),(19,25,8,4,'2022-03-01',5),(20,16,4,13,'2022-03-02',3),(21,7,5,3,'2022-03-05',5),(22,3,17,9,'2022-03-06',5),(23,11,12,14,'2022-03-07',4),(24,14,10,12,'2022-03-07',2),(25,20,23,10,'2022-03-09',3),(26,15,14,16,'2022-03-10',2),(27,26,9,11,'2022-03-13',4),(28,24,19,1,'2022-03-17',4),(29,27,15,15,'2022-03-20',3),(30,28,11,6,'2022-03-25',2),(31,30,16,1,'2022-03-26',3),(32,31,35,2,'2022-03-30',2),(33,35,22,3,'2022-04-02',3),(34,32,36,5,'2022-04-03',1),(35,34,26,4,'2022-04-06',1),(36,32,3,4,'2022-04-07',1),(37,36,6,3,'2022-04-10',3),(38,33,30,8,'2022-04-12',2);
/*!40000 ALTER TABLE `shipping` ENABLE KEYS */;
UNLOCK TABLES;

--
-- Final view structure for view `count_game_sales`
--

/*!50001 DROP VIEW IF EXISTS `count_game_sales`*/;
/*!50001 SET @saved_cs_client          = @@character_set_client */;
/*!50001 SET @saved_cs_results         = @@character_set_results */;
/*!50001 SET @saved_col_connection     = @@collation_connection */;
/*!50001 SET character_set_client      = utf8mb4 */;
/*!50001 SET character_set_results     = utf8mb4 */;
/*!50001 SET collation_connection      = utf8mb4_0900_ai_ci */;
/*!50001 CREATE ALGORITHM=UNDEFINED */
/*!50013 DEFINER=`Leek`@`%` SQL SECURITY DEFINER */
/*!50001 VIEW `count_game_sales` AS select `customer_order`.`game_id` AS `game_id`,count(`customer_order`.`game_id`) AS `count` from `customer_order` group by `customer_order`.`game_id` order by `count` desc */;
/*!50001 SET character_set_client      = @saved_cs_client */;
/*!50001 SET character_set_results     = @saved_cs_results */;
/*!50001 SET collation_connection      = @saved_col_connection */;

--
-- Final view structure for view `customer_more_than_one`
--

/*!50001 DROP VIEW IF EXISTS `customer_more_than_one`*/;
/*!50001 SET @saved_cs_client          = @@character_set_client */;
/*!50001 SET @saved_cs_results         = @@character_set_results */;
/*!50001 SET @saved_col_connection     = @@collation_connection */;
/*!50001 SET character_set_client      = utf8mb4 */;
/*!50001 SET character_set_results     = utf8mb4 */;
/*!50001 SET collation_connection      = utf8mb4_0900_ai_ci */;
/*!50001 CREATE ALGORITHM=UNDEFINED */
/*!50013 DEFINER=`Leek`@`%` SQL SECURITY DEFINER */
/*!50001 VIEW `customer_more_than_one` AS select concat(`c`.`c_first_name`,' ',`c`.`c_last_name`) AS `customer`,count(0) AS `quantity`,concat('$ ',convert(format(sum(`g`.`price`),2) using utf8mb4)) AS `item_total` from (((`game` `g` join `customer_order` `co` on((`g`.`game_id` = `co`.`game_id`))) join `customer` `c` on((`c`.`customer_id` = `co`.`customer_id`))) join `publisher` `p` on((`g`.`publisher_id` = `p`.`publisher_id`))) group by `customer` having (count(0) > 1) order by `customer` desc */;
/*!50001 SET character_set_client      = @saved_cs_client */;
/*!50001 SET character_set_results     = @saved_cs_results */;
/*!50001 SET collation_connection      = @saved_col_connection */;

--
-- Final view structure for view `customer_order_count`
--

/*!50001 DROP VIEW IF EXISTS `customer_order_count`*/;
/*!50001 SET @saved_cs_client          = @@character_set_client */;
/*!50001 SET @saved_cs_results         = @@character_set_results */;
/*!50001 SET @saved_col_connection     = @@collation_connection */;
/*!50001 SET character_set_client      = utf8mb4 */;
/*!50001 SET character_set_results     = utf8mb4 */;
/*!50001 SET collation_connection      = utf8mb4_0900_ai_ci */;
/*!50001 CREATE ALGORITHM=UNDEFINED */
/*!50013 DEFINER=`Leek`@`%` SQL SECURITY DEFINER */
/*!50001 VIEW `customer_order_count` AS select concat(`c`.`c_first_name`,' ',`c`.`c_last_name`) AS `customer`,replace(replace(replace(`c`.`phone_number`,') ','-'),'(',''),'-','-') AS `customer_phone_number`,count(0) AS `quantity`,`g`.`game_title` AS `game_title`,`g`.`esrb_rating` AS `esrb_rating`,`p`.`publisher_name` AS `publisher_name`,`s`.`confirmation_number` AS `confirmation_number`,`s`.`shipped_date` AS `shipped_date`,concat('$ ',convert(format(sum(`g`.`price`),2) using utf8mb4)) AS `item_total` from ((((`game` `g` join `customer_order` `co` on((`g`.`game_id` = `co`.`game_id`))) join `customer` `c` on((`c`.`customer_id` = `co`.`customer_id`))) join `publisher` `p` on((`g`.`publisher_id` = `p`.`publisher_id`))) join `shipping` `s` on((`g`.`game_id` = `s`.`game_id_ship`))) group by `customer` order by `customer` desc */;
/*!50001 SET character_set_client      = @saved_cs_client */;
/*!50001 SET character_set_results     = @saved_cs_results */;
/*!50001 SET collation_connection      = @saved_col_connection */;

--
-- Final view structure for view `games_below_40`
--

/*!50001 DROP VIEW IF EXISTS `games_below_40`*/;
/*!50001 SET @saved_cs_client          = @@character_set_client */;
/*!50001 SET @saved_cs_results         = @@character_set_results */;
/*!50001 SET @saved_col_connection     = @@collation_connection */;
/*!50001 SET character_set_client      = utf8mb4 */;
/*!50001 SET character_set_results     = utf8mb4 */;
/*!50001 SET collation_connection      = utf8mb4_0900_ai_ci */;
/*!50001 CREATE ALGORITHM=UNDEFINED */
/*!50013 DEFINER=`Leek`@`%` SQL SECURITY DEFINER */
/*!50001 VIEW `games_below_40` AS select `g`.`game_title` AS `game_title`,`g`.`price` AS `price` from `game` `g` where (`g`.`price` < 40) */;
/*!50001 SET character_set_client      = @saved_cs_client */;
/*!50001 SET character_set_results     = @saved_cs_results */;
/*!50001 SET collation_connection      = @saved_col_connection */;

--
-- Final view structure for view `publisher_and_retailer_info`
--

/*!50001 DROP VIEW IF EXISTS `publisher_and_retailer_info`*/;
/*!50001 SET @saved_cs_client          = @@character_set_client */;
/*!50001 SET @saved_cs_results         = @@character_set_results */;
/*!50001 SET @saved_col_connection     = @@collation_connection */;
/*!50001 SET character_set_client      = utf8mb4 */;
/*!50001 SET character_set_results     = utf8mb4 */;
/*!50001 SET collation_connection      = utf8mb4_0900_ai_ci */;
/*!50001 CREATE ALGORITHM=UNDEFINED */
/*!50013 DEFINER=`Leek`@`%` SQL SECURITY DEFINER */
/*!50001 VIEW `publisher_and_retailer_info` AS select distinct `g`.`game_title` AS `game_title`,`c`.`game_platforms` AS `game_platforms`,`p`.`publisher_name` AS `publisher_name`,`gt`.`retailer_name` AS `retailer_name`,concat(`gt`.`retailer_city`,', ',`gt`.`retailer_state`) AS `retailer city/state`,concat(`e`.`first_name`,' ',`e`.`last_name`) AS `employee`,replace(replace(replace(`gt`.`retailer_phone_number`,') ','-'),'(',''),'-','-') AS `retailer_phone_number` from (((((`game_retailers` `gt` join `game` `g` on((`gt`.`retailer_id` = `g`.`retailer_id`))) join `publisher` `p` on((`g`.`publisher_id` = `p`.`publisher_id`))) join `console_platform` `c` on((`c`.`console_platform_id` = `g`.`console_id`))) join `shipping` `s` on((`gt`.`retailer_id` = `s`.`emp_id_ship`))) join `employee` `e` on((`e`.`retailer_id_1` = `gt`.`retailer_id`))) */;
/*!50001 SET character_set_client      = @saved_cs_client */;
/*!50001 SET character_set_results     = @saved_cs_results */;
/*!50001 SET collation_connection      = @saved_col_connection */;
/*!40103 SET TIME_ZONE=@OLD_TIME_ZONE */;

/*!40101 SET SQL_MODE=@OLD_SQL_MODE */;
/*!40014 SET FOREIGN_KEY_CHECKS=@OLD_FOREIGN_KEY_CHECKS */;
/*!40014 SET UNIQUE_CHECKS=@OLD_UNIQUE_CHECKS */;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
/*!40111 SET SQL_NOTES=@OLD_SQL_NOTES */;

-- Dump completed on 2022-05-10 18:38:03
