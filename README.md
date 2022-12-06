# EdubridgeProject
Edubridge Final Group Project


Database
Database name : smartcontact
Tables 
1) contact : CREATE TABLE `contact` (
  `cid` int NOT NULL,
  `description` longtext,
  `email` varchar(255) DEFAULT NULL,
  `image` varchar(255) DEFAULT NULL,
  `name` varchar(255) DEFAULT NULL,
  `phone` varchar(255) DEFAULT NULL,
  `second_name` varchar(255) DEFAULT NULL,
  `work` varchar(255) DEFAULT NULL,
  `user_id` int DEFAULT NULL,
  PRIMARY KEY (`cid`),
  KEY `FKe07k4jcfdophemi6j1lt84b61` (`user_id`),
  CONSTRAINT `FKe07k4jcfdophemi6j1lt84b61` FOREIGN KEY (`user_id`) REFERENCES `user` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;


2) hibernate_sequence : CREATE TABLE `hibernate_sequence` (
  `next_val` bigint DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

3) user : CREATE TABLE `user` (
  `id` int NOT NULL,
  `about` varchar(500) DEFAULT NULL,
  `email` varchar(255) DEFAULT NULL,
  `enabled` bit(1) NOT NULL,
  `image_url` varchar(255) DEFAULT NULL,
  `name` varchar(20) DEFAULT NULL,
  `password` varchar(255) DEFAULT NULL,
  `role` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `UK_ob8kqyqqgmefl0aco34akdtpe` (`email`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
