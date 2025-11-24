# Railwaystations
api for railway-stations.org train station map site
# main
```cpp
#include "Railwaystations.h"
#include <iostream>

int main() {
   Railwaystations api;

    auto stats = api.get_stats().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    stats.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```


