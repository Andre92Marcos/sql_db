**Connect to a remote db**

    mvn -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:update -Dliquibase.contexts=dev

**Clear all Checksums**

	mvn liquibase:clearCheckSums

**Rollbacks to a specific tag**

	mvn liquibase:rollback -Dliquibase.rollbackTag=tag_id


**Generate Update SQL**

    mvn -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:updateSQL

	Output will be created to target\liquibase\migrate.sql




**Examples:**

    mvn -DvarDB='nyx_dev' -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:update

    mvn -DvarDB='nyx_dev' -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:rollback -Dliquibase.rollbackTag='bms-logic-db-schema-0'

    mvn -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:clearCheckSums

    mvn ' -Dliquibase.url='jdbc:sqlserver://localhost:1433;databaseName=nyx_dev' -Dliquibase.password=q clean compile liquibase:updateSQL


