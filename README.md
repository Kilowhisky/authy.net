# Authy .NET

Authy.Net is a simple client for the Authy API.

Forked and patched from the library of devinmartin in [https://bitbucket.org/devinmartin/authy.net/wiki/Home](https://bitbucket.org/devinmartin/authy.net/wiki/Home)


## License

This is released under an MIT license. See the file LICENSE.txt for more information.

## Documentation
The API is really simple and corresponds to the [Authy Documentation]

Create an instance of the client. You must provide your API key and indicate if this is to run in test mode or not.

```
var client = new AuthyClient("my key", test:false);
```

Any errors returned by the API will in turn throw a corresponding exception (see list of all exceptions and their corresponding error code in `ErrorHelper.cs`. In case of no failure, all methods will return a result object specific to the call. There is always a Message property and a RawResponse property, which can be used to get additional information when debugging problems but generally isn't needed in actual code.


### The statuses are:
1. Success
2. BadRequest
3. Unauthorized
    * This can mean that your API key is invalid or that the provided token is invalid. Once your integration has been
      tested it likely means that the token is invalid but the raw response will provide more info.
4. ServiceUnavailable


## Configuration instructions

### 1. Install mercurial

Type the following command in the terminal:

    $ brew install mercurial

### 2. Download and install Mono MDK

From this link: [http://www.mono-project.com/download/] (http://www.mono-project.com/download/)

### 3. Download and install the Xamarin IDE

From this link: [http://www.monodevelop.com/download/] (http://www.monodevelop.com/download/)

### 4. Import the project in Xamarin Studio

Open -> Authy.Net.sln

## Copyright

Copyright (c) 2015-2020 Authy Inc. See LICENSE.txt for further details.
