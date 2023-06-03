# Flutter-HelloWorld

## Flutter
https://zenn.dev/kazutxt/books/flutter_practice_introduction
この手順書でのHelloWorldまで通す

## Amplify
https://docs.amplify.aws/start/q/integration/flutter/
基本この手順書に従う

### Configure the Amplify CLI
```
amplify configure
```
### Create a new Flutter application
HelloWorldを作っているのでPASS
```
#flutter create budget_tracker
```

### Add Amplify to your application
pubspec.yamlをUpdate
```
name: helloworld
description: A new Flutter project.
environment:
  sdk: ">=2.18.0 <3.0.0"

dependencies:
  amplify_api: ^1.0.0
  amplify_auth_cognito: ^1.0.0
  amplify_authenticator: ^1.0.0
  amplify_flutter: ^1.0.0
  flutter:
    sdk: flutter
  go_router: ^6.5.5
```

依存関係をInstall
```
flutter pub get
```

### Platform Setup
Web対応を考えているので、対象外

### Configure the Amplify CLI
```
% amplify init
Note: It is recommended to run this command from the root of your app directory
? Enter a name for the project helloworld
The following configuration will be applied:

Project information
| Name: helloworld
| Environment: dev
| Default editor: Visual Studio Code
| App type: flutter
| Configuration file location: ./lib/

? Initialize the project with the above configuration? Yes
Using default provider  awscloudformation
? Select the authentication method you want to use: AWS profile

For more information on AWS Profiles, see:
https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html

? Please choose the profile you want to use default
```

### Hosting
https://docs.aws.amazon.com/amplify/latest/userguide/getting-started.html
記載内容に従いフロント画面をAmplifyにHosting
