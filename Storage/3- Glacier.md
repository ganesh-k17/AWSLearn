# Glacier:

* Archivaldata storage
* Fractions of a penny per GB/month
* Three access methods (data retreival)
	- Expedited (3-5 minutes)
	- Standard (3-5 hours)
	- Bulk (5-12 hours)
* Key is to pick the right kind of access methods
* You define the region for data storage
* Data stored wih AES 256-bit encryption
* We can setup a vault and store data

## Glacier Integration:

* S3 Cold data can be automatically moved into Glacier
* Snow devices can be used to import data
* Storage gateway can connect to Glacier

## Glacier Concepts:

* Archive (but in S3 its called Objects)
* Vaults
* Vault locks
* Data Retrieval:
	- Up to 5% retrieved at no charge, no rollover month to month
	- Vault can be configured to limit costs

## Other Details:

* A Single AWS account can create up to 1000 vaults per region
* Only empty vaults can be deleted
* Glacier supports multipart uploads of archives, so a large archive is not required to be uploaded in a single action.