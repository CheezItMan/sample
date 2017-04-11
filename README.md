# sample



```ruby
class Vehicle < ApplicationRecord
  belongs_to :owner
  validates :vin, uniqueness: true

  def similar_vehicles
    return Vehicle.where(["make = ? and model = ?", make, model])
  end
end
```

```ruby
class Owner < ApplicationRecord
  validates :name, presence: true
  has_many :vehicles
end
```


```bash
$ rails routes
Prefix Verb   URI Pattern             Controller#Action
       DELETE /vehicles/:id(.:format) vehicles#destroy
```

```ruby
require "test_helper"

describe VehiclesController do
  # your code here
end
```
