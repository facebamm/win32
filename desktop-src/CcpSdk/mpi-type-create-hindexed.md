---
Description: 'Defines a new data type that consists of a specified number of blocks of arbitrary size.'
audience: developer
author: 'REDMOND\\danlep'
manager: 'REDMOND\\timlt'
ms.assetid: '07b5a612-29be-46f9-b91e-1cbc387baf78'
ms.prod: 'windows-server-dev'
ms.technology: 'compute-cluster-pack'
ms.tgt_platform: multiple
title: 'MPI\_Type\_create\_hindexed function'
---

# MPI\_Type\_create\_hindexed function

Defines a new data type that consists of a specified number of blocks of arbitrary size. Each block is a concatenation of elements of an existing data type. Each block can contain a different number of elements and have a different displacement.

## Syntax


```C++
int MPIAPI MPI_Type_create_hindexed(
  ������int �����������������������count,
  ������_In_count_(count) int �����array_of_blocklengths[],
  ������_In_count_(count) MPI_Aint array_of_displacements[],
  ������MPI_Datatype ��������������oldtype,
  _Out_�MPI_Datatype ��������������*newtype
);
```



## Parameters

<dl> <dt>

*count* 
</dt> <dd>

The number of blocks and the number of entries in the *array\_of\_blocklengths* and *array\_of\_displacements* parameters.

</dd> <dt>

*array\_of\_blocklengths* 
</dt> <dd>

The number of elements of each block.

</dd> <dt>

*array\_of\_displacements* 
</dt> <dd>

The displacement of each block in bytes.

</dd> <dt>

*oldtype* 
</dt> <dd>

The MPI data type of each element.

</dd> <dt>

*newtype* \[out\]
</dt> <dd>

On return, contains an [**MPI\_Datatype**](mpi-datatype.md) handle that represents the new data type.

</dd> </dl>

## Return value

Returns **MPI\_SUCCESS** on success. Otherwise, the return value is an error code.

In Fortran, the return value is stored in the *IERROR* parameter.

## Fortran

``` syntax
MPI_TYPE_CREATE_HINDEXED(COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR)
    COUNT, ARRAY_OF_BLOCKLENGTHS, ARRAY_OF_DISPLACEMENTS, OLDTYPE, NEWTYPE, IERROR
```

## Remarks

This function replaces the [**MPI\_Type\_hindexed**](mpi-type-hindexed.md), which is deprecated.

## Requirements



|                    |                                                                                                                                                                                          |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Product<br/> | HPC Pack 2012 MS-MPI Redistributable Package, HPC Pack 2008 R2 MS-MPI Redistributable Package, HPC Pack 2008 MS-MPI Redistributable Package or HPC Pack 2008 Client Utilities<br/> |
| Header<br/>  | <dl> <dt>Mpi.h; </dt> <dt>Mpif.h</dt> </dl>                                           |
| Library<br/> | <dl> <dt>Msmpi.lib</dt> </dl>                                                                                                     |
| DLL<br/>     | <dl> <dt>Msmpi.dll</dt> </dl>                                                                                                     |



## See also

<dl> <dt>

[MPI Datatype Functions](mpi-datatype-functions.md)
</dt> <dt>

[**MPI\_Type\_indexed**](mpi-type-indexed.md)
</dt> </dl>

�

�



