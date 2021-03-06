<small>Piwik\DataTable\Filter\</small>

MetadataCallbackReplace
=======================

Execute a callback for each row of a DataTable passing certain column values and metadata as metadata, and replaces row metadata with the callback result.

**Basic usage example**

    $dataTable->filter('MetadataCallbackReplace', array('url', function ($url) {
        return $url . '#index';
    }));

Methods
-------

The class defines the following methods:

- [`__construct()`](#__construct) &mdash; Constructor.
- [`filter()`](#filter) &mdash; See [ColumnCallbackReplace](/api-reference/Piwik/DataTable/Filter/ColumnCallbackReplace). Inherited from [`ColumnCallbackReplace`](../../../Piwik/DataTable/Filter/ColumnCallbackReplace.md)
- [`enableRecursive()`](#enablerecursive) &mdash; Enables/Disables recursive filtering. Inherited from [`BaseFilter`](../../../Piwik/DataTable/BaseFilter.md)
- [`filterSubTable()`](#filtersubtable) &mdash; Filters a row's subtable, if one exists and is loaded in memory. Inherited from [`BaseFilter`](../../../Piwik/DataTable/BaseFilter.md)

<a name="__construct" id="__construct"></a>
<a name="__construct" id="__construct"></a>
### `__construct()`

Constructor.

#### Signature

-  It accepts the following parameter(s):
    - `$table` ([`DataTable`](../../../Piwik/DataTable.md)) &mdash;
      
    - `$metadataToFilter` (`array`|`string`) &mdash;
       The metadata whose values should be passed to the callback and then replaced with the callback's result.
    - `$functionToApply` (`callable`) &mdash;
       The function to execute. Must take the column value as a parameter and return a value that will be used to replace the original.
    - `$functionParameters` (`array`|`null`) &mdash;
       deprecated - use an [anonymous function](http://php.net/manual/en/functions.anonymous.php) instead.
    - `$extraColumnParameters` (`array`) &mdash;
       Extra column values that should be passed to the callback, but shouldn't be replaced.

<a name="filter" id="filter"></a>
<a name="filter" id="filter"></a>
### `filter()`

See [ColumnCallbackReplace](/api-reference/Piwik/DataTable/Filter/ColumnCallbackReplace).

#### Signature

-  It accepts the following parameter(s):
    - `$table` ([`DataTable`](../../../Piwik/DataTable.md)) &mdash;
      
- It does not return anything or a mixed result.

<a name="enablerecursive" id="enablerecursive"></a>
<a name="enableRecursive" id="enableRecursive"></a>
### `enableRecursive()`

Enables/Disables recursive filtering. Whether this property is actually used
is up to the derived BaseFilter class.

#### Signature

-  It accepts the following parameter(s):
    - `$enable` (`bool`) &mdash;
      
- It does not return anything or a mixed result.

<a name="filtersubtable" id="filtersubtable"></a>
<a name="filterSubTable" id="filterSubTable"></a>
### `filterSubTable()`

Filters a row's subtable, if one exists and is loaded in memory.

#### Signature

-  It accepts the following parameter(s):
    - `$row` ([`Row`](../../../Piwik/DataTable/Row.md)) &mdash;
       The row whose subtable should be filter.
- It does not return anything or a mixed result.

