# cHashTable

A hash table class for Dataflex that supports values of any type, from basic types to structs and arrays. Since the Dataflex standard library doesn't include a dictionary type, you are free and safe to download and use this library if you need one. It's been around since 2013 and is actively maintained in 2021.

Supported and tested on DataFlex 14.1-20.0, it most likely works on more versions.

If you are using DataFlex 14.1-18.0, add a use statement for [DFCompatibilityLayer](https://github.com/ekstrom/DFCompatibilityLayer). It includes the function StringToUCharArray, which does not exist in DataFlex 14.1-18.0.

## Code Examples

```dataflex
Use cHashTable.pkg

...

Handle hHashTable
String sValue
String[] saKeys

// cHashTable is a Class and can be instantiated in any way supported by Dataflex
Get Create U_cHashTable to hHashTable

// Use the Set and Get keywords to store and access data
Set Value of hHashTable "Key" to "Value"
Get Value of hHashTable "Key" to sValue

// Use the Keys function to get an array of all keys that currently exist
Get Keys of hHashTable to saKeys

// Use the Clear procedure to clear all entries
Send Clear of hHashTable

// Finally, don't forget to deallocate!
Send Destroy of hHashTable
```
