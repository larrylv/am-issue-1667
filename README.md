``` bash
$ bundle install
$ cat console
#!/usr/bin/env ruby

require 'bundler'
Bundler.setup

require 'activemerchant'

credit_card = ActiveMerchant::Billing::CreditCard.new(
    number: '4111111111111111',
    month: 12,
    year: 18,
    first_name: 'Test',
    last_name: 'User',
    verification_value: '123'
  )

require 'pry'; binding.pry
$ ./console
```
