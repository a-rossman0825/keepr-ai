## Database

### Tables:
- accounts (User Profiles with Auth0 authentication)
- keeps (Image posts with metadata)
- vaults (Collections/folders for organizing keeps)
- vault_keep (Many-to-Many relationship between vaults *and* keeps)

### Database Migrations
- Create and apply Entity Framework migrations whenever schema changes occur.
- Entity Framework Migrations should follow a 'commit message' naming convention/style.

 ---