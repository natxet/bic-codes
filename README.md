# bic-codes
First, create the table:

```mysql
CREATE TABLE IF NOT EXISTS `swift` (
  `id` smallint(5) unsigned NOT NULL AUTO_INCREMENT,
  `country_id` char(2) CHARACTER SET latin1 NOT NULL DEFAULT 'ES',
  `bank_code` char(4) CHARACTER SET latin1 NOT NULL DEFAULT '',
  `swift` char(11) CHARACTER SET latin1 NOT NULL,
  `bank_name` varchar(255) CHARACTER SET latin1 DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `country_id_and_bank_code` (`country_id`,`bank_code`)
) ENGINE=InnoDB;
```

Then execute the SQL to insert the codes, you will find the SQL in the data directory of this repository. For instance [Spanish banks](data/es.sql)

LAST UPDATED: 2016-03-07
