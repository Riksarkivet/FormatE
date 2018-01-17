# cdf

## identifier
| type              | value
| ----------------- | -----
| alias             | [cdf](#common-data-format)
| alias             | [cdfml](#common-data-format-markup-language)
| alias             | [Common Data Format](#common-data-format)
| alias             | [Common Data Format Markup Language](#common-data-format-markup-language)

# Common Data Format

## identifier
| type                    | value
| ----------------------- | -----
| file extension          | cdf

* https://spdf.gsfc.nasa.gov/pub/software/cdf/doc/cdf364/cdf36ifd.pdf

## CDF 3.0
| type | value | comment
| ---- | ----- | -------
| signature | `0xCD 0xF3 0x00 0x01` | The first 4 bytes; big-endian unsigned integer at offset `0x0000000000000000`.
| signature | `0x00 0x00 0xFF 0xFF` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for a CDF without compression or with only selected variables compressed. The internal record starts at offset `0x0000000000000008`.
| signature | `0xCC 0xCC 0x00 0x01` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for compressed CDF. The internal record starts at offset `0x0000000000000008`.

## CDF 2.7
| type | value | comment
| ---- | ----- | -------
| signature | `0xCD 0xF2 0x60 0x02` | The first 4 bytes; big-endian unsigned integer at offset `0x0000000000000000`.
| signature | `0x00 0x00 0xFF 0xFF` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for a CDF without compression or with only selected variables compressed. The internal record starts at offset `0x0000000000000008`.
| signature | `0xCC 0xCC 0x00 0x01` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for compressed CDF. The internal record starts at offset `0x0000000000000008`.

## CDF 2.6
| type | value | comment
| ---- | ----- | -------
| signature | `0xCD 0xF2 0x60 0x02` | The first 4 bytes; big-endian unsigned integer at offset `0x0000000000000000`.
| signature | `0x00 0x00 0xFF 0xFF` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for a CDF without compression or with only selected variables compressed. The internal record starts at offset `0x0000000000000008`.
| signature | `0xCC 0xCC 0x00 0x01` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004` for compressed CDF. The internal record starts at offset `0x0000000000000008`.

## CDF <2.6
| type | value | comment
| ---- | ----- | -------
| signature | `0x00 0x00 0xFF 0xFF` | The first 4 bytes; big-endian unsigned integer at offset `0x0000000000000000`.
| signature | `0x00 0x00 0xFF 0xFF` | The second 4 bytes; big-endian unsigned integer at offset `0x0000000000000004`. The functionality compression is not available for CDF 2.6 and earlier. The internal record starts at offset `0x0000000000000008`.

## CDF Markup Language

* https://cdf.gsfc.nasa.gov/html/cdfml.html
