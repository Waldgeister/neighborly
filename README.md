# Neighbor.ly [![Build Status](https://secure.travis-ci.org/catarse/catarse.png?branch=master)](https://travis-ci.org/catarse/catarse) [![Coverage Status](https://coveralls.io/repos/catarse/catarse/badge.png?branch=channels)](https://coveralls.io/r/catarse/catarse) [![Dependency Status](https://gemnasium.com/catarse/catarse.png)](https://gemnasium.com/catarse/catarse)

Welcome to the first open source fundraising toolkit for community projects. Neighbor.ly began in April 2012 as a fork of the wildly successful Brazillian crowdfunding platform [Catarse](https://github.com/catarse/catarse). Working closely with the developers of that project, Neighbor.ly is building towards a full spectrum fundraising toolkit for civic projects. 

## An open source fundraising toolkit for civic projects

Welcome to Catarse's source code repository. Our goal with opening the source code is to stimulate the creation of a community of developers around a high-quality crowdfunding platform.

You can see the software in action at http://neighbor.ly.

## Getting started

## Internationalization

This software was first created as Brazil's first crowdfunding platform. 
Thus, it was first made in Portuguese and with a brazilian payment gateway. 
We are now internationalizing it, and already have a good support for the english language and for paypal express checkout.
See below the Payment gateways section for more information about integrating Catarse with a payment system of your choice.
If you want to join us in this effort, please feel free to fork the repository and send us a pull request with your changes. If you have *any* doubt, please join our Google Group at http://groups.google.com/group/catarse-dev and we will help you.

### Translations

We hope to support a lot of languages in the future. So we are willing to accept pull requests with translations to other languages. Here's a small guide to translate Catarse to your language in a way that we can integrate your translation in the main repository:
* TODO 

Thanks a lot to Daniel Walmsley, from http://purpose.com, for starting the internationalization and beginning the english translation.

## Payment gateways

Neighbor.ly supports payment gateways through payment engines. Payment engines are extensions to Neighbor.ly that implement a specific payment gateway logic. 
The two current supported payment gateways are:
* Authorize.net for credit cards and e-checks
* PayPal

We have plans to implement Dwolla in the future.

If you have created another payment engine, please contact us so we can link your engine here.



## How to contribute with code

Before contributing, take a look at our Roadmap (https://www.pivotaltracker.com/projects/427075) and discuss your plans in our mailing list (http://groups.google.com/group/catarse-dev).

Our pivotal is concerned with user visible features using user stories. But we do have some features not visible to users that are planned such as:
* Turn Catarse into a Rails Engine with customizable views.
* Turn Backer model into a finite state machine using the state_machine gem as we did with the Project model.
* Improve the payments engine isolation providing a clear API to integrate new payment engines in the backer review page.
* Make a installer script to guide users through initial Catarse configuration.

Currently, a lot of functionality is not tested. If you don't know how to start contributing, please help us regaining control over the code and write a few tests for us! *Any* doubt, please join our Google Group at http://groups.google.com/group/catarse-dev and we will help you out.

After that, just fork the project, change what you want, and send us a pull request.

### Coding style
* We prefer the `{foo: 'bar'}` over `{:foo => 'bar'}`
* We prefer the `->(foo){ bar(foo) }` over `lambda{|foo| bar(foo) }`

### Best practices (or how to get your pull request accepted faster)

We use RSpec and Steak for the tests, and the best practices are:
* Create one acceptance tests for each scenario of the feature you are trying to implement.
* Create model and controller tests to keep 100% of code coverage at least in the new parts that you are writing.
* Feel free to add specs to the code that is already in the repository without the proper coverage ;)
* Try to isolate models from controllers as best as you can.
* Regard the existing tests for a style guide, we try to use implicit spec subjects and lazy evaluation as often as we can. 

## Credits

Author: Daniel Weinmann

Contributors: You know who you are ;) The commit history can help, but the list was getting bigger and pointless to keep in the README.

## License

Copyright (c) 2011 Softa

Licensed under the MIT license (see MIT-LICENSE file)
