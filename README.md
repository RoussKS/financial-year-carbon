# \RoussKS\FinancialYear\CarbonAdapter - Carbon Adapter for RoussKS Financial Year PHP Library

[![Latest Version](https://img.shields.io/github/release/RoussKS/financial-year-carbon.svg?style=flat-square)](https://github.com/RoussKS/financial-year-carbon/releases)
[![Build Status](https://travis-ci.org/RoussKS/financial-year-carbon.svg?branch=master)](https://travis-ci.org/RoussKS/financial-year-carbon)
[![codecov](https://codecov.io/gh/RoussKS/financial-year-carbon/branch/master/graph/badge.svg)](https://codecov.io/gh/RoussKS/financial-year-carbon)
[![GitHub license](https://img.shields.io/github/license/RoussKS/financial-year-carbon.svg)](https://github.com/RoussKS/financial-year-carbon/blob/master/LICENSE)

### General Details

This is the [Carbon](https://github.com/briannesbitt/carbon) Adapter for the [RoussKS\FinancialYear](https://github.com/roussks/financial-year).

The library internally transforms, handles and returns Carbon Immutable Objects only.

Introduction, limitations and generic functionality is the same as the parent and described in [RoussKS\FinancialYear readme](https://github.com/RoussKS/financial-year/blob/master/README.md).

### Requirements
- PHP Version ^7.1 ( 7.1 =< PHP Version =< 7.x.x according to [Composer docs version constraints](https://getcomposer.org/doc/articles/versions.md#caret-version-range-) )

### Installation
```console
composer require roussks/financial-year-carbon
```

### Basic Use
```php
require_once __DIR__ . '/vendor/autoload.php';

// CarbonAdapter
// If instantiating with string, it must be of ISO-8601 format 'YYYY-MM-DD'
$startDate = new \Carbon\Carbon::createFromDate('2019-01-01');

$fy = new \RoussKS\FinancialYear\CarbonAdapter('calendar', $startDate);

echo $fy->getFyEndDate()->toDateString(); // 2019-12-31 
```

### Versioning
The current library will be using [Semantic Versioning](https://semver.org/)

As it relies on the parent's [RoussKS\FinancialYear](https://github.com/roussks/financial-year) Interface, it will limit versioning to MINOR releases.
Hence, when the parent class has a new feature and upgrades the PATCH version, the current library will remain in the Minor version until the new feature is implemented.

Non-breaking changes will result in a MINOR or a PATCH version update as classified by SemVer.

Major version releases will not guarantee backwards compatibility.