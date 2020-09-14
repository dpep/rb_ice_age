IceAge
======

Freeze your ENVironment for testing.

#### Install
```gem install ice_age```


#### Usage
```ruby
require 'ice_age'

describe 'Feature' do
  context 'with new feature enabled' do
    before { ENV['FEATURE_ENABLED'] = 'true' }

    it { expect(ENV['FEATURE_ENABLED']).to eq 'true' }

    # run tests against enabled feature
  end

  # ENV resets
  it { expect(ENV['FEATURE_ENABLED']).to be_nil }

  # run tests when feature is disabled
end
```

----
![Gem](https://img.shields.io/gem/dt/ice_age?style=plastic)
