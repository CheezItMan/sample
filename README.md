# sample



```ruby
class Vehicle < ApplicationRecord
  belongs_to :owner
  validates :vin, uniqueness: true
end
```

```ruby
class Owner < ApplicationRecord
  validates :name, presence: true
  has_many :vehicles
end
```
