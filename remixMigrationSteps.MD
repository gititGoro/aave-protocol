
# Importing into Remix
Use Firefox browser. The compiler in Remix sometimes crashes in other browsers
1. You'll need to create a blank file in Remix. This allows you to add directories
2. Create all the top level directories and treat the node dependecies like openzeppelin-solidity as a top level contract
3. Add the subdirectories. At this point you shouldn't have added any code.
4. Add the files and copy in the code.
5. Remember to change the openzeppelin-solidity import references to use relative paths.
6. Compile each file to check that you've imported correctly. 
   ->pro tip: when you get an error about a contract having already been declared, look at the import above the offending line. Go to that file. One of the imports in this file has an incorrect path

# Deploying to Kovan from remix
The first step to deploying is to find the innermost contract in the Aave architecture. In Aave there's a contract registry that is deployed once. All the contracts reference this registry contract to retrieve the correct versions of their dependencies.

To deploy, click on the deploy menu option (1) and set Environment to Injected Web3 (2). This will prompt your metamask to connect to Remix.

![](./remixMigrationImages/Deploy.png)


Deploy LendingPoolAddressesProvider.sol:
Your deployed contract will be displayed in a list. 


![](./remixMigrationImages/copy-address.png)


Click the copy icon to retrieve the address. Don't worry about ABIs. The repository has them already.

  **Note: all deployments happening from 0x4011Ba13ACD2E078B0234C125D04e5C61803D07d. Since many of these contracts are owned, ownership transfer will have to occur at some point.**


```
 LendingPoolAddressesProvider Kovan address: 0x52D581f9fD911AA7A06ca10b234887877Dd7d397
```

dfsdfs
