**mvn liquibase:clearCheckSums**

	Clears ALL checksums in the current changelog, so they will be recalculated next update.

**mvn liquibase:rollback -Dliquibase.rollbackTag=tag_id**

	Rollbacks to a specific tag