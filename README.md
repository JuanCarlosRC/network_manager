Inspired by NoScopeDevs [network_manager](https://github.com/NoScopeDevs/network_manager) implementation using internet_connection_checker

[![Package Test](https://github.com/JuanCarlosRC/network_manager/actions/workflows/package_test.yml/badge.svg?branch=master&event=label)](https://github.com/JuanCarlosRC/network_manager/actions/workflows/package_test.yml)

- ✅  Null Safety
- ✅  Clean Architecture 
- ✅  Basic Testing

## Usage

```dart
Future<void> main() async {
  final internetConnectionChecker = InternetConnectionChecker();
  final networkManager = NetworkManager(internetConnectionChecker);

  logResult(await networkManager.isOnline);

  networkManager.isOnlineStream
      .take(1)
      .listen((isOnline) => logResult(isOnline));
}

void logResult(bool isOnline) {
  if (isOnline) {
    log('We are online! 😎');
  } else {
    log('We are offline... 😓');
  }
}
```


