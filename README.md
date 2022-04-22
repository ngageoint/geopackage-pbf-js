## @ngageoint/geopackage-pbf-js &mdash; Convert your PBF to a GeoPackage

This utility will convert between PBF and GeoPackage using the NGA GeoPackage JS library.

### Installation ###

[![NPM](https://img.shields.io/npm/v/@ngageoint/geopackage-pbf-js.svg)](https://www.npmjs.com/package/@ngageoint/geopackage-pbf-js)

```sh
$ npm install @ngageoint/geopackage-pbf-js
```

### Usage

#### Command Line

```sh
./cli /path/to/file/to/convert.pbf /path/to/file/to/create.gpkg
```

#### Javascript
```javascript
const { PBFToGeoPackage } = require('@ngageoint/geopackage-pbf-js');
const pbfFile = './test.pbf';
const geoPackageFile = './test.gpkg';
const tableName = 'features';

// Convert PBF to GeoPackage feature table
const converter = new PBFToGeoPackage();
converter.convert({ pbf: pbfFile, geoPackage: geoPackageFile, tableName: tableName }).then(() => {
  console.log('File conversion complete');
  console.log('Converted %s to %s', pbfFile, geoPackageFile);
});
```

#### GeoPackage JS Library ####

The [GeoPackage Libraries](http://ngageoint.github.io/GeoPackage/) were developed at the [National Geospatial-Intelligence Agency (NGA)](http://www.nga.mil/) in collaboration with [BIT Systems](http://www.bit-sys.com/). The government has "unlimited rights" and is releasing this software to increase the impact of government investments by providing developers with the opportunity to take things in new directions. The software use, modification, and distribution rights are stipulated within the [MIT license](http://choosealicense.com/licenses/mit/).

### Pull Requests ###
If you'd like to contribute to this project, please make a pull request. We'll review the pull request and discuss the changes. All pull request contributions to this project will be released under the MIT license.

Software source code previously released under an open source license and then modified by NGA staff is considered a "joint work" (see 17 USC § 101); it is partially copyrighted, partially public domain, and as a whole is protected by the copyrights of the non-government authors and must be released according to the terms of the original open source license.


### Changelog


##### 4.1.0
- Update to GeoPackage JS 4.1.0.
