# sample



```ruby
class Vehicle < ApplicationRecord
  belongs_to :owner
  validates :vin, uniqueness: true
end
```
