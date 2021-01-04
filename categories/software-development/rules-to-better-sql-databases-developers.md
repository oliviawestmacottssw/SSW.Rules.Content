---
type: category
title: Rules To Better SQL Databases - Developers
guid: c66da635-3483-4287-9d19-013152b12d0f
uid: rules-to-better-sql-databases-developers
index:
- data-do-you-not-allow-nulls-in-text-fields
- data-do-you-not-allow-nulls-in-number-fields-if-it-has-the-same-meaning-as-zero
- data-do-you-avoid-spaces-and-empty-lines-at-the-start-of-character-columns
- data-do-you-use-identities-in-sql-server
- data-dates-do-you-make-sure-you-have-valid-date-data-in-your-database
- data-dates-do-you-know-datetime-fields-must-be-converted-to-universal-time
- data-do-you-use-temporal-tables-to-audit-data-changes
- data-do-you-avoid-invalid-characters-in-object-identifiers
- do-you-have-a-general-contact-detail-table
- data-do-you-use-a-url-instead-of-an-image-in-your-database
- schema-do-you-only-use-unicode-datatypes-nchar-nvarchar-and-ntext-in-special-circumstances
- schema-do-you-always-use-varchar
- schema-do-you-have-standard-tables-and-columns
- schema-do-you-use-bit-numeric-data-type-correctly
- schema-do-you-use-natural-or-surrogate-primary-keys
- schema-do-you-create-primary-key-on-your-tables
- schema-do-you-create-clustered-index-on-your-tables
- schema-do-you-avoid-using-indexes-on-rowguid-column
- schema-do-you-have-a-rowversion-column
- schema-do-you-use-fillfactor-of-90-for-indexes-and-constraints
- schema-do-you-always-have-version-tracking-tables
- schema-do-you-use-computed-columns-rather-than-denormalized-fields
- schema-do-you-use-triggers-for-denormalized-fields
- schema-do-you-validate-each-denormalized-field-with-procvalidate
- schema-do-you-avoid-using-user-schema-separation
- schema-do-you-create-a-consistent-primary-key-column-on-your-tables
- schema-do-you-use-separate-lookup-tables-rather-than-one-large-lookup-table-for-your-lookup-data
- schema-do-you-know-how-to-provide-best-database-schema-document
- schema-do-you-add-zs-prefix-to-system-tables
- views-do-you-avoid-having-views-as-redundant-objects
- stored-procedures-do-you-keep-your-stored-procedures-simple
- stored-procedures-do-you-return-a-value-indicating-the-status
- stored-procedures-do-you-standardize-the-return-values-of-stored-procedures-for-success-and-failures
- stored-procedures-do-you-use-output-parameters-if-you-need-to-return-the-value-of-variables
- stored-procedures-do-you-check-the-global-variable-error-after-executing-a-data-manipulation-statement
- stored-procedures-do-you-use-scope_identity-to-get-the-most-recent-row-identity
- stored-procedures-do-you-set-nocount-on-for-production-and-nocount-off-off-for-development-debugging-purposes
- stored-procedures-do-you-avoid-starting-user-stored-procedures-with-system-prefix-sp_-or-dt_
- stored-procedures-do-you-avoid-using-select-when-inserting-data
- stored-procedures-do-you-use-transactions-for-complicated-stored-procedures
- stored-procedures-do-you-use-error-handling-in-your-stored-procedures
- stored-procedures-do-you-know-sql-stored-procedure-names-should-be-prefixed-with-the-owner
- relationships-do-you-turn-on-referential-integrity-in-relationships
- relationships-do-you-use-update-cascade-when-creating-a-relationship
- relationships-do-you-avoid-using-cascade-delete
- relationships-do-you-set-not-for-replication-when-creating-a-relationship
- relationships-do-you-have-foreign-key-constraints-on-columns-ending-with-id
- general-do-you-know-object-name-should-not-be-a-reserved-word
- general-do-you-know-object-name-should-not-contain-spaces
- general-do-you-know-to-not-use-sp_rename-to-rename-objects
- general-do-you-know-object-name-should-follow-your-company-naming-conventions
- general-do-you-use-a-sql-server-object-naming-standard
- general-do-you-use-a-sql-server-stored-procedure-naming-standard
- general-do-you-use-a-sql-server-indexes-naming-standard
- general-do-you-use-a-sql-server-relationship-naming-standard
- general-do-you-know-the-naming-convention-for-use-on-database-server-test-and-production
- middle-tier-do-you-implement-business-logic-in-middle-tier
- do-you-parameterize-all-input-to-your-database
- views-do-you-use-sql-views
- data-do-you-avoid-empty-lines-at-the-start-of-character-columns
- schema-do-you-use-less-than-24-characters-for-table-names
- middle-tier-do-you-submit-all-dates-to-sql-server-in-iso-format

---
Here are some of the typical things that all SQL Server DBAs and Database developers should know. These rules are above and beyond the most basic textbook recommendations of:


▪   Ensuring your databases are Normalized and in 3rd Normal Form 


▪   Making sure you have primary keys, foreign keys and simple indexes to improve performance 


▪   Making sure you Back up regularly 


▪   Basic Naming conventions (see some of our object naming conventions)


▪   Minimizing result set sizes and data over the wire

Link: [Database Coding Standard and Guideline](http&#58;//www.nyx.net/~bwunder/dbChangeControl/standard.htm).





If you still need help, [visit our SQL Server Database consulting page](https&#58;//www.ssw.com.au/ssw/Consulting/Database-Development.aspx) and book in a consultant.

