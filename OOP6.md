```cpp
#include "seven_twelve.h"
#include <iostream>

SevenTwelve::SevenTwelve(const std::vector<YellowTag> &all_items) {
  // add code here
  for(int i =0; i < all_items.size(); i++){
    allitems.push_back(all_items[i]);
  }

  // for(int i = 0; i < allitems.size(); i++){
  //   std::cout << i << "all_items_name = " << allitems[i].name << '\n';
  //   std::cout << i << "all_items_price = " << allitems[i].price << '\n';
  // }
}

std::vector<std::string> SevenTwelve::GetAffordableList(AllMember customer) {
  // add code here
  std::vector<std::string> Ans = {};

  for (int i = 0; i < allitems.size(); i++) {

    // for(int i = 0; i < allitems.size(); i++){
    //   std::cout << i << "all_items_name = " << allitems[i].name << '\n';
    //   std::cout << i << "all_items_price = " << allitems[i].price << '\n';
    // }

    if(customer.points >= allitems[i].price){
      Ans.push_back(allitems[i].name);
      customer.points -= allitems[i].price;
    }
  }
  // for(int i = 0;i < Ans.size(); i++){
  //   std::cout << i << "distance_ = " << Ans[i] << '\n';
  // }
  return Ans;
}

std::vector<std::string> Shopping(const std::vector<YellowTag> &all_items,
                                  AllMember customer) {
  SevenTwelve shop(all_items);
  return shop.GetAffordableList(customer);
}

// int main(){

//   std::cout << "Hello = " << '\n';

//   std::vector<YellowTag> shopping_list = {
//     {"snack", 20},
//     {"drink", 30},
//     {"candy", 10},
//     {"chocolate", 50} };

//   AllMember{1, 100};


//   return 0;
// }
```

```cpp
#include "Travel.h"
#include <cmath>    // for std::abs
#include <iostream> // optional, for debugging or output

Travels::Travels(std::vector<double> destination) {
    destination_ = destination;
}

void Travels::calculatedistance() {
    distance.clear();
    if (!destination.empty()) {
        // First segment is from A to first destination
        distance.pushback(destination[0]);

        // Next segments are between consecutive destinations
        for (sizet i = 1; i < destination.size(); ++i) {
            double segment = std::abs(destination[i] - destination[i - 1]);
            distance_.push_back(segment);
        }
    }
}

// Helper function to compute cost for a single segment
double compute_cost(double d) {
    double cost = 0.0;

    if (d <= 5.0) {
        cost += d * 5.0;
    }
    else if (d <= 10.0) {
        cost += 5.0 * 5.0 + (d - 5.0) * 8.0;
    }
    else {
        cost += 5.0 * 5.0 + 5.0 * 8.0 + (d - 10.0) * 4.5;
    }

    return cost;
}

void Travels::calculate_cost() {
    totalcost = 0.0;

    for (double d : distance_) {
        totalcost += compute_cost(d);
    }
}
```