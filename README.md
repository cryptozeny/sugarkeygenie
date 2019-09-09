# sugarkeygenie

## Disclaimer

**This project was written in May 2013 for educational purposes.**

**Modern cryptocurrency wallets should use hierarchical deterministic (HD) keys instead.**

## Introduction

sugarkeygenie is a standalone Sugarchain keypair/address generator written in Go.
sugarkeygenie generates an ECDSA secp256k1 keypair, dumps the public key in
compressed and uncompressed Sugarchain address, hexadecimal and base64 formats,
and dumps the private key in Wallet Import Format (WIF), Wallet Import Format
Compressed (WIFC), hexadecimal and base64 formats.

sugarkeygenie includes a lightweight Go package called btckey to easily generate
keypairs, and convert them between compressed and uncompressed varieties of
Sugarchain Address, Wallet Import Format and raw bytes.

See documentation on btckey here: https://godoc.org/github.com/vsergeev/btckeygenie/btckey

Donations are welcome at :  
`15PKyTs3jJ3Nyf3i6R7D9tfGCY1ZbtqWdv` vsergeev  
`31hMrody48EpQF4ZH3eFEd7CMJLPPCBHSe` cryptozeny  
:-)

## Usage

#### Generating a new keypair

    $ ./sugarkeygenie
    Sugarchain Address (Compressed)        SZLpPiWoCFrU6qbrhXRa9gHgvnWWY7RLxi
    Public Key Bytes (Compressed)       03FA00404779643781AD794808AA7775FD1CF263A0C1119DF6D167D7C63D9A3FDD
    Public Key Base64 (Compressed)      A/oAQEd5ZDeBrXlICKp3df0c8mOgwRGd9tFn18Y9mj/d

    Sugarchain Address (Uncompressed)      Sk6oFeoN9CsexL6N1FHvbrwJMAdn8VoGmx
    Public Key Bytes (Uncompressed)     04FA00404779643781AD794808AA7775FD1CF263A0C1119DF6D167D7C63D9A3FD
                                        D991B3E132FB932E391418233DDE5D2A258BB4786B5CAB9D1FC975D3F01207877
    Public Key Base64 (Uncompressed)    BPoAQEd5ZDeBrXlICKp3df0c8mOgwRGd9tFn18Y9mj/dmRs+Ey+5MuORQYIz3eXSoli7R4a1yrnR/JddPwEgeHc=

    Private Key WIFC (Compressed)       L26rxz3jtHjmVfriFzf5nDYYyYVetwaXXrXFfNXhfJEieAsxS82G
    Private Key WIF (Uncompressed)      5JvSNJ1AiXXXvczUvhFX5oo7ntYQzXwiosBw5AQiqYzwJ3gp8Hh
    Private Key Bytes                   91A9EF35E676BA25BE8FE86CA0B3A1F081717894F6079B858797E3CB726D0BB3
    Private Key Base64                  kanvNeZ2uiW+j+hsoLOh8IFxeJT2B5uFh5fjy3JtC7M=
    $

#### Importing an existing WIF/WIFC
https://github.com/cryptozeny/bitzeny-vanitygen/tree/da485eb438d1579935856bf262a85758fa1fea40

    $ ./sugarkeygenie 5JSVT8jWHvX3dfdnDGucmVmL5nc9ZC6Hu5Ji2jKVjKc2U65NJgK
    Sugarchain Address (Compressed)        SRurMB7RbDJB8JCnVp4Qrxzu8bnFBSuKXe
    Public Key Bytes (Compressed)       02E78D566BC5A54A12D5FB96963036C47262BEE0B07FACB77E5B85EA0CFD8ABB44
    Public Key Base64 (Compressed)      AueNVmvFpUoS1fuWljA2xHJivuCwf6y3fluF6gz9irtE

    Sugarchain Address (Uncompressed)      SUGARyQweBrpDTWe9Tq1CNgEWz5Xm1nEX7
    Public Key Bytes (Uncompressed)     04E78D566BC5A54A12D5FB96963036C47262BEE0B07FACB77E5B85EA0CFD8ABB4
                                        4570CBF75B16B2458A4B01D5DFC517956DF156ADB0AF7394AA570B4D1269EDFBE
    Public Key Base64 (Uncompressed)    BOeNVmvFpUoS1fuWljA2xHJivuCwf6y3fluF6gz9irtEVwy/dbFrJFiksB1d/FF5Vt8VatsK9zlKpXC00Sae374=

    Private Key WIFC (Compressed)       KyyWaM8cHhDccqXLZBDEsPxfE8J8m5xMar1A6dndoo7bUCVHmqcs
    Private Key WIF (Uncompressed)      5JSVT8jWHvX3dfdnDGucmVmL5nc9ZC6Hu5Ji2jKVjKc2U65NJgK
    Private Key Bytes                   5235041C5A1DEF793FB9481020BA5F49CCEDAB6536D2B0870230CA0F90250659
    Private Key Base64                  UjUEHFod73k/uUgQILpfScztq2U20rCHAjDKD5AlBlk=
    $

#### Help/Usage

    $ sugarkeygenie -h
    Usage: sugarkeygenie [WIF/WIFC]
    
    sugarkeygenie v1.0.0 - https://github.com/cryptozeny/sugarkeygenie
    $

## Installation

To fetch, build and install sugarkeygenie to `$GOPATH/bin`:

    $ go get github.com/cryptozeny/sugarkeygenie

## License

sugarkeygenie is MIT licensed. See the included `LICENSE` file for more details.
