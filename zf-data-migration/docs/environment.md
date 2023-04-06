## Environment

### Local Test

As you go you want to set up a local test environment to
test as you build your migration workbook.

For this I usually do the bare minimum:
- create a local database. There is a simple mysql script called "create zfm db.sql" in the
zfm repo.  You need to edit the first two lines before running it.
- run a zfm server this requires a config file, 
  - For the first run of the program use TYPEORM_SYNC_DATABASE=true so the database will be generated
  - For further runs, use TYPEORM_SYNC_DATABASE=false
  - Use the setting HIDE_IMPORT_TOOL=false, so you can use the Import tool.
  This should be set to false in production
  - in the zf-server directory npm run start:prod => this will create all the db tables
  - data fill the mutation_types and screenType tables with the obvious sql scripts from the zfm repo
- run the zfm client - just ng serve rather than configuring and running Apache

