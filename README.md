# bic-codes
First, create the table:

```mysql
CREATE TABLE IF NOT EXISTS `bic_codes` (
  `id` smallint(5) unsigned NOT NULL AUTO_INCREMENT,
  `country_code` char(2) CHARACTER SET latin1 NOT NULL DEFAULT 'ES',
  `country_bank_number` char(4) CHARACTER SET latin1 NOT NULL DEFAULT '',
  `bic_code` char(11) CHARACTER SET latin1 NOT NULL,
  `bank_name` varchar(255) CHARACTER SET latin1 DEFAULT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `country_bank_number` (`country_code`,`country_bank_number`)
) ENGINE=InnoDB;
```

Then execute the SQL to insert the codes, you will find the SQL in the data directory of this repository. For instance [Spanish banks](data/es.sql)

LAST UPDATED: 2016-03-07
