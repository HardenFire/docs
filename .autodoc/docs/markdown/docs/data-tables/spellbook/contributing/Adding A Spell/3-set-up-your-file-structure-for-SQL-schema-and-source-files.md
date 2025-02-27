[View code on GitHub](https://dune.com/docs/data-tables/spellbook/contributing/Adding A Spell/3-set-up-your-file-structure-for-SQL-schema-and-source-files.md)

This app technical guide provides instructions on how to set up the file structure for SQL, schema, and source files in the Dune Docs project. The guide explains that all Spells are stored in the `/spellbook/models` directory by project name, then blockchain network. The folder names are all lowercase, and words are separated by underscores. The guide provides an example of the folder structure for the Keep3r network, where the folder is `/spellbook/models/keep3r_network/ethereum`. 

The guide explains that if the project folder exists but a Spell is being created for a new blockchain, a folder for the new blockchain should be created. The guide then explains that three files need to be created: a `.sql` file for the Spell's logic, a `_schema.yml` file to define the Spell's purpose and add generic tests, descriptions, metadata, etc., and a `_sources.yml` file with any project-specific table dependencies. The guide provides an example of the file structure for a Spell folder.

The guide also explains the naming convention for Spell files. Schema files are named `[project_name]_[blockchain]_schema.yml`, sources files are named `[project_name]_[blockchain]_sources.yml`, and SQL files for Spells are named `[project_name]_[blockchain]_[spell_name].sql`. 

The guide then provides an example of a specific v1 migration example where three additional `.sql` files are needed for a Spell called `keep3r_network_ethereum_view_job_log.sql`. The guide explains that these files are needed because the original `view_job_log.sql` V1 Abstraction has two `FROM` statements that reference two other files that are also abstractions that need to be converted into Spells. The guide also explains that a recursive check needs to be done to see if those abstractions depend on any other abstractions that have yet to be migrated to Spells. 

Overall, this app technical guide provides a detailed explanation of how to set up the file structure for Spells in the Dune Docs project and provides examples to help users understand the process.
## Questions: 
 1. What is the purpose of the dune docs app and how does it relate to blockchain SQL analysis?
- The app technical guide does not provide information on the purpose of the dune docs app or its relation to blockchain SQL analysis.

2. What is the file structure for storing Spells in the dune docs app?
- Spells are stored in the `/spellbook/models` directory by project name, then blockchain network. Names are all lower case and words are separated by `_`. The app requires the creation of three files: a `.sql` file for the Spell's logic, a `_schema.yml` file for defining the spell's purpose and adding metadata, and a `_sources.yml` file for project-specific table dependencies.

3. How does the app handle dependencies between Spells and abstractions in the migration process?
- The app requires a recursive check to see if abstractions depend on any other abstractions that have yet to be migrated to Spells. The app also requires the creation of additional `.sql` files for Spells that depend on other abstractions, and these dependencies are identified by searching for `FROM` statements in the original abstractions.