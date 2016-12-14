# OIN Metadata Specification

[![Join the chat at https://gitter.im/openimagerynetwork/oin-metadata-spec](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/openimagerynetwork/oin-metadata-spec?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Any S3 buckets listed in the [Register](https://github.com/openimagerynetwork/register) will need to follow a specification to enable valid indexing within a catalog instance. A metadata file is required for each image file in the bucket. An image file is an RGB GeoTIFF.This repository contains the metadata specification. 

## Sample file

See [sample.json](sample.json)

## Specification Description 

| element | type | name | description | 
| --- | --- | --- | --- | 
| uuid | string | File | unique URI to file | 
| projection | string | Projection | CRS of the datasource in full WKT format | 
| bbox | array | Bounding Box | Pair of min and max coordinates in CRS units, (min_x, min_y, max_x, max_y) | 
| footprint | string | Datasource footprint | WKT format, describing the actual footprint of the imagery | 
| gsd | number | Ground Spatial Distance | Average ground spatial distance (resolution) of the datasource imagery, expressed in meters | 
| file_size | number | File Size | File size on disk in bytes | 
| acquisition_start | string | Acquisition Date Start | First date of acquisition in UTC (Combined date and time representation) | 
| acquisition_end | string | Acquisition Date End | Last date of acquisition in UTC (Combined date and time representation) (optional) | 
| title | string | Title | Human friendly title of the image | 
| platform_name | string | Name of platform | Examples: WorldView 3 or eBee RTK | 
| platform_type | string | Type of platform | List of possible platform sources limited to satellite, aircraft, UAV, balloon, kite |  
| provider | string | Imagery Provider | Provider/owner of the OIN bucket | 
| contact | string | Contact | Name and email address of the data provider | 
| properties | object | Properties | Additional properties about the image (optional) | 
