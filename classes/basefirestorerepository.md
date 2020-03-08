
# Class: BaseFirestoreRepository <**T**>

## Type parameters

▪ **T**: *[IEntity](../interfaces/ientity.md)*

## Hierarchy

  ↳ [AbstractFirestoreRepository](abstractfirestorerepository.md)‹T›

  ↳ **BaseFirestoreRepository**

  ↳ [BandRepository](bandrepository.md)

## Implements

* [IBaseRepository](../interfaces/ibaserepository.md)‹T, this› & [IQueryable](../interfaces/iqueryable.md)‹T, this› & [IOrderable](../interfaces/iorderable.md)‹T, this› & [ILimitable](../interfaces/ilimitable.md)‹T, this› & [IQueryExecutor](../interfaces/iqueryexecutor.md)‹T, this›
* [IBaseRepository](../interfaces/ibaserepository.md)‹T, this› & [IQueryable](../interfaces/iqueryable.md)‹T, this› & [IOrderable](../interfaces/iorderable.md)‹T, this› & [ILimitable](../interfaces/ilimitable.md)‹T, this› & [IQueryExecutor](../interfaces/iqueryexecutor.md)‹T, this›

## Index

### Constructors

* [constructor](basefirestorerepository.md#constructor)

### Properties

* [colMetadata](basefirestorerepository.md#protected-colmetadata)
* [colName](basefirestorerepository.md#protected-colname)
* [collectionPath](basefirestorerepository.md#protected-collectionpath)
* [config](basefirestorerepository.md#protected-config)
* [firestoreColRef](basefirestorerepository.md#private-firestorecolref)
* [subColMetadata](basefirestorerepository.md#protected-subcolmetadata)

### Methods

* [create](basefirestorerepository.md#create)
* [createBatch](basefirestorerepository.md#createbatch)
* [delete](basefirestorerepository.md#delete)
* [execute](basefirestorerepository.md#execute)
* [extractTFromColSnap](basefirestorerepository.md#protected-extracttfromcolsnap)
* [extractTFromDocSnap](basefirestorerepository.md#protected-extracttfromdocsnap)
* [find](basefirestorerepository.md#find)
* [findById](basefirestorerepository.md#findbyid)
* [findOne](basefirestorerepository.md#findone)
* [initializeSubCollections](basefirestorerepository.md#protected-initializesubcollections)
* [limit](basefirestorerepository.md#limit)
* [orderByAscending](basefirestorerepository.md#orderbyascending)
* [orderByDescending](basefirestorerepository.md#orderbydescending)
* [runTransaction](basefirestorerepository.md#runtransaction)
* [toSerializableObject](basefirestorerepository.md#protected-toserializableobject)
* [transformFirestoreTypes](basefirestorerepository.md#protected-transformfirestoretypes)
* [update](basefirestorerepository.md#update)
* [validate](basefirestorerepository.md#validate)
* [whereArrayContains](basefirestorerepository.md#wherearraycontains)
* [whereEqualTo](basefirestorerepository.md#whereequalto)
* [whereGreaterOrEqualThan](basefirestorerepository.md#wheregreaterorequalthan)
* [whereGreaterThan](basefirestorerepository.md#wheregreaterthan)
* [whereLessOrEqualThan](basefirestorerepository.md#wherelessorequalthan)
* [whereLessThan](basefirestorerepository.md#wherelessthan)

## Constructors

###  constructor

\+ **new BaseFirestoreRepository**(`colName`: string, `collectionPath?`: string): *[BaseFirestoreRepository](basefirestorerepository.md)*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[constructor](abstractfirestorerepository.md#constructor)*

*Defined in [BaseFirestoreRepository.ts:22](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L22)*

**Parameters:**

Name | Type |
------ | ------ |
`colName` | string |
`collectionPath?` | string |

**Returns:** *[BaseFirestoreRepository](basefirestorerepository.md)*

## Properties

### `Protected` colMetadata

• **colMetadata**: *[CollectionMetadata](../interfaces/collectionmetadata.md)*

*Inherited from [TransactionRepository](transactionrepository.md).[colMetadata](transactionrepository.md#protected-colmetadata)*

*Defined in [AbstractFirestoreRepository.ts:30](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L30)*

___

### `Protected` colName

• **colName**: *string*

*Inherited from [TransactionRepository](transactionrepository.md).[colName](transactionrepository.md#protected-colname)*

*Defined in [AbstractFirestoreRepository.ts:31](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L31)*

___

### `Protected` collectionPath

• **collectionPath**: *string*

*Inherited from [TransactionRepository](transactionrepository.md).[collectionPath](transactionrepository.md#protected-collectionpath)*

*Defined in [AbstractFirestoreRepository.ts:33](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L33)*

___

### `Protected` config

• **config**: *[MetadataStorageConfig](../interfaces/metadatastorageconfig.md)*

*Inherited from [TransactionRepository](transactionrepository.md).[config](transactionrepository.md#protected-config)*

*Defined in [AbstractFirestoreRepository.ts:32](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L32)*

___

### `Private` firestoreColRef

• **firestoreColRef**: *CollectionReference*

*Defined in [BaseFirestoreRepository.ts:22](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L22)*

___

### `Protected` subColMetadata

• **subColMetadata**: *[CollectionMetadata](../interfaces/collectionmetadata.md)[]*

*Inherited from [TransactionRepository](transactionrepository.md).[subColMetadata](transactionrepository.md#protected-subcolmetadata)*

*Defined in [AbstractFirestoreRepository.ts:29](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L29)*

## Methods

###  create

▸ **create**(`item`: T): *Promise‹T›*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[create](abstractfirestorerepository.md#abstract-create)*

*Defined in [BaseFirestoreRepository.ts:43](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L43)*

**Parameters:**

Name | Type |
------ | ------ |
`item` | T |

**Returns:** *Promise‹T›*

___

###  createBatch

▸ **createBatch**(): *[FirestoreBatchSingleRepository](firestorebatchsinglerepository.md)‹T›*

*Defined in [BaseFirestoreRepository.ts:109](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L109)*

**Returns:** *[FirestoreBatchSingleRepository](firestorebatchsinglerepository.md)‹T›*

___

###  delete

▸ **delete**(`id`: string): *Promise‹void›*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[delete](abstractfirestorerepository.md#abstract-delete)*

*Defined in [BaseFirestoreRepository.ts:90](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L90)*

**Parameters:**

Name | Type |
------ | ------ |
`id` | string |

**Returns:** *Promise‹void›*

___

###  execute

▸ **execute**(`queries`: Array‹[IFireOrmQueryLine](../interfaces/ifireormqueryline.md)›, `limitVal?`: number, `orderByObj?`: [IOrderByParams](../interfaces/iorderbyparams.md), `single?`: boolean): *Promise‹T[]›*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[execute](abstractfirestorerepository.md#abstract-execute)*

*Defined in [BaseFirestoreRepository.ts:119](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L119)*

**Parameters:**

Name | Type |
------ | ------ |
`queries` | Array‹[IFireOrmQueryLine](../interfaces/ifireormqueryline.md)› |
`limitVal?` | number |
`orderByObj?` | [IOrderByParams](../interfaces/iorderbyparams.md) |
`single?` | boolean |

**Returns:** *Promise‹T[]›*

___

### `Protected` extractTFromColSnap

▸ **extractTFromColSnap**(`q`: QuerySnapshot): *T[]*

*Inherited from [TransactionRepository](transactionrepository.md).[extractTFromColSnap](transactionrepository.md#protected-extracttfromcolsnap)*

*Defined in [AbstractFirestoreRepository.ts:118](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L118)*

**Parameters:**

Name | Type |
------ | ------ |
`q` | QuerySnapshot |

**Returns:** *T[]*

___

### `Protected` extractTFromDocSnap

▸ **extractTFromDocSnap**(`doc`: DocumentSnapshot): *T*

*Inherited from [TransactionRepository](transactionrepository.md).[extractTFromDocSnap](transactionrepository.md#protected-extracttfromdocsnap)*

*Defined in [AbstractFirestoreRepository.ts:102](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L102)*

**Parameters:**

Name | Type |
------ | ------ |
`doc` | DocumentSnapshot |

**Returns:** *T*

___

###  find

▸ **find**(): *Promise‹T[]›*

*Inherited from [TransactionRepository](transactionrepository.md).[find](transactionrepository.md#find)*

*Defined in [AbstractFirestoreRepository.ts:282](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L282)*

Execute the query and applies all the filters (if specified)

**`memberof`** AbstractFirestoreRepository

**Returns:** *Promise‹T[]›*

List of documents that matched the filters
(if specified)

___

###  findById

▸ **findById**(`id`: string): *Promise‹T›*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[findById](abstractfirestorerepository.md#abstract-findbyid)*

*Defined in [BaseFirestoreRepository.ts:36](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L36)*

**Parameters:**

Name | Type |
------ | ------ |
`id` | string |

**Returns:** *Promise‹T›*

___

###  findOne

▸ **findOne**(): *Promise‹T | null›*

*Inherited from [TransactionRepository](transactionrepository.md).[findOne](transactionrepository.md#findone)*

*Defined in [AbstractFirestoreRepository.ts:295](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L295)*

Execute the query to find at least one document matching all
filters (if specified)

**`memberof`** AbstractFirestoreRepository

**Returns:** *Promise‹T | null›*

One document that matched the filters
(if specified), or null if none exists.

___

### `Protected` initializeSubCollections

▸ **initializeSubCollections**(`entity`: T): *void*

*Inherited from [TransactionRepository](transactionrepository.md).[initializeSubCollections](transactionrepository.md#protected-initializesubcollections)*

*Defined in [AbstractFirestoreRepository.ts:88](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L88)*

**Parameters:**

Name | Type |
------ | ------ |
`entity` | T |

**Returns:** *void*

___

###  limit

▸ **limit**(`limitVal`: number): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [BaseFirestoreRepository](basefirestorerepository.md).[limit](basefirestorerepository.md#limit)*

*Defined in [AbstractFirestoreRepository.ts:237](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L237)*

Returns a new QueryBuilder with a maximum number of results
to return. Can only be used once per query.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`limitVal` | number | maximum number of results to return Must be greater or equal than 0 |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

QueryBuilder A new QueryBuilder with
the specified limit applied

___

###  orderByAscending

▸ **orderByAscending**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [BaseFirestoreRepository](basefirestorerepository.md).[orderByAscending](basefirestorerepository.md#orderbyascending)*

*Defined in [AbstractFirestoreRepository.ts:257](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L257)*

Returns a new QueryBuilder with an additional ascending order
specified by @param prop. Can only be used once per query.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be ordered on, where prop could be keyof T or a lambda where T is the first parameter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
ordering applied.

___

###  orderByDescending

▸ **orderByDescending**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [BaseFirestoreRepository](basefirestorerepository.md).[orderByDescending](basefirestorerepository.md#orderbydescending)*

*Defined in [AbstractFirestoreRepository.ts:271](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L271)*

Returns a new QueryBuilder with an additional descending order
specified by @param prop. Can only be used once per query.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be ordered on, where prop could be keyof T or a lambda where T is the first parameter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
ordering applied.

___

###  runTransaction

▸ **runTransaction**<**R**>(`executor`: function): *Promise‹R›*

*Defined in [BaseFirestoreRepository.ts:95](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L95)*

**Type parameters:**

▪ **R**

**Parameters:**

▪ **executor**: *function*

▸ (`tran`: [TransactionRepository](transactionrepository.md)‹T›): *Promise‹R›*

**Parameters:**

Name | Type |
------ | ------ |
`tran` | [TransactionRepository](transactionrepository.md)‹T› |

**Returns:** *Promise‹R›*

___

### `Protected` toSerializableObject

▸ **toSerializableObject**(`obj`: T): *Object*

*Inherited from [TransactionRepository](transactionrepository.md).[toSerializableObject](transactionrepository.md#protected-toserializableobject)*

*Defined in [AbstractFirestoreRepository.ts:67](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L67)*

**Parameters:**

Name | Type |
------ | ------ |
`obj` | T |

**Returns:** *Object*

___

### `Protected` transformFirestoreTypes

▸ **transformFirestoreTypes**(`obj`: T): *T*

*Inherited from [TransactionRepository](transactionrepository.md).[transformFirestoreTypes](transactionrepository.md#protected-transformfirestoretypes)*

*Defined in [AbstractFirestoreRepository.ts:70](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L70)*

**Parameters:**

Name | Type |
------ | ------ |
`obj` | T |

**Returns:** *T*

___

###  update

▸ **update**(`item`: T): *Promise‹T›*

*Overrides [AbstractFirestoreRepository](abstractfirestorerepository.md).[update](abstractfirestorerepository.md#abstract-update)*

*Defined in [BaseFirestoreRepository.ts:74](https://github.com/wovalle/fireorm/blob/5547513/src/BaseFirestoreRepository.ts#L74)*

**Parameters:**

Name | Type |
------ | ------ |
`item` | T |

**Returns:** *Promise‹T›*

___

###  validate

▸ **validate**(`item`: T): *Promise‹ValidationError[]›*

*Inherited from [TransactionRepository](transactionrepository.md).[validate](transactionrepository.md#validate)*

*Defined in [AbstractFirestoreRepository.ts:305](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L305)*

Uses class-validator to validate an entity using decorators set in the collection class

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`item` | T | class or object representing an entity |

**Returns:** *Promise‹ValidationError[]›*

An array of class-validator errors

___

###  whereArrayContains

▸ **whereArrayContains**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereArrayContains](transactionrepository.md#wherearraycontains)*

*Defined in [AbstractFirestoreRepository.ts:220](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L220)*

Returns a new QueryBuilder with a filter specifying that the
value in @param val must be contained in @param prop.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.

___

###  whereEqualTo

▸ **whereEqualTo**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereEqualTo](transactionrepository.md#whereequalto)*

*Defined in [AbstractFirestoreRepository.ts:133](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L133)*

Returns a new QueryBuilder with a filter specifying that the
value in @param prop must be equal to @param val.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.

___

###  whereGreaterOrEqualThan

▸ **whereGreaterOrEqualThan**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereGreaterOrEqualThan](transactionrepository.md#wheregreaterorequalthan)*

*Defined in [AbstractFirestoreRepository.ts:166](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L166)*

Returns a new QueryBuilder with a filter specifying that the
value in @param prop must be greater or equal than @param val.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.

___

###  whereGreaterThan

▸ **whereGreaterThan**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereGreaterThan](transactionrepository.md#wheregreaterthan)*

*Defined in [AbstractFirestoreRepository.ts:148](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L148)*

Returns a new QueryBuilder with a filter specifying that the
value in @param prop must be greater than @param val.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.

___

###  whereLessOrEqualThan

▸ **whereLessOrEqualThan**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereLessOrEqualThan](transactionrepository.md#wherelessorequalthan)*

*Defined in [AbstractFirestoreRepository.ts:202](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L202)*

Returns a new QueryBuilder with a filter specifying that the
value in @param prop must be less or equal than @param val.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.

___

###  whereLessThan

▸ **whereLessThan**(`prop`: [IWherePropParam](../globals.md#iwherepropparam)‹T›, `val`: [IFirestoreVal](../globals.md#ifirestoreval)): *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

*Inherited from [TransactionRepository](transactionrepository.md).[whereLessThan](transactionrepository.md#wherelessthan)*

*Defined in [AbstractFirestoreRepository.ts:184](https://github.com/wovalle/fireorm/blob/5547513/src/AbstractFirestoreRepository.ts#L184)*

Returns a new QueryBuilder with a filter specifying that the
value in @param prop must be less than @param val.

**`memberof`** AbstractFirestoreRepository

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`prop` | [IWherePropParam](../globals.md#iwherepropparam)‹T› | field to be filtered on, where prop could be keyof T or a lambda where T is the first parameter |
`val` | [IFirestoreVal](../globals.md#ifirestoreval) | value to compare in the filter |

**Returns:** *[IQueryBuilder](../globals.md#iquerybuilder)‹T›*

A new QueryBuilder with the specified
query applied.