# SecureStore

[![Version](https://img.shields.io/github/release/RobertoMachorro/SecureStore.svg)](https://github.com/RobertoMachorro/SecureStore/releases)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

This is **yet another** [Keychain Services](https://developer.apple.com/documentation/security/keychain_services) wrapper - queue the eye roll. I tried out quite a number, they felt overly abstracted, underimplemented or confusing. Even [Apple has one](https://developer.apple.com/library/archive/samplecode/GenericKeychain/Introduction/Intro.html). I liked Sam Soffes' [SAMKeychain](https://github.com/soffes/SAMKeychain), but it only supports [kSecClassGenericPassword](https://developer.apple.com/documentation/security/ksecclassgenericpassword). In particular, I was looking for [kSecClassInternetPassword](https://developer.apple.com/documentation/security/ksecclassinternetpassword). [SecureStore](https://github.com/RobertoMachorro/SecureStore) supports both very well and can expand to other types (certificates, keys, identities, etc).

The goal was to pickup a good project and adapt it as necessary, I don't like to re-invent wheels, and found one written by [Lorenzo Boaro](https://twitter.com/flexaddicted), it's part of [RayWenderlich.com](https://rayWenderlich.com) tutorial [Keychain Services API Tutorial for Passwords in Swift](https://www.raywenderlich.com/9240-keychain-services-api-tutorial-for-passwords-in-swift). Unfortunately, neither the author nor the project where on *GitHub*. Also, the project - while written multiplatform - only targeted iOS. I highly recommend Lorenzo's post, it describes the *Keychain* operation very well.

So this code / Framework starts where its predecessor left off, by taking the pristine sources and enhancing / adapting for real life Framework usage. *Please note that the original copyright and permission has been kept, as requested by the author*. If you are interested in the process and adapting of the code, take a look at the *commit log*.

## Adding To Your Project

Swift Package Manager is in the works. Right now Carthage is the way to go:

> github "RobertoMachorro/SecureStore"

Check the tests for call examples, most are very atomic.

## Project Status

Currently, the project is ready to use and defaults to macOS builds.

## Pending

* iOS Target
* macOS and passes all but 2 tests. The original source passes all tests under iOS.

## Changes from Original Source

* Independent project and framework with shared schema for Carthage
* Public Queryable structs initializers

## Contributing

Feel free to fork a copy and create a pull request.

## Documentation

Both API documentation and examples plus a patient description of [Keychain Services](https://developer.apple.com/documentation/security/keychain_services) can be found at [Keychain Services API Tutorial for Passwords in Swift](https://www.raywenderlich.com/9240-keychain-services-api-tutorial-for-passwords-in-swift).
