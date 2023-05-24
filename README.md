# Welcome to MAKO IoT
MAKO IoT is a platform for building IoT applications based on .NET. It leverages the power of C# language and software best practices. It is based on [.NET nanoFramework](https://www.nanoframework.net/)

The goal of MAKO IoT is to provide:
* across-the-board development experience with highest software industry standard best practices
* building blocks for common tasks / functionalities
* templates and boilerplate which make doing right things easy and doing wrong things hard
* tools & practices

# Build your app with MAKO IoT

## Pre-requisites
- Install [.NET nanoFramework](https://docs.nanoframework.net/content/getting-started-guides/index.html)

## Code your project
Create two [nanoFramework projects](https://docs.nanoframework.net/content/getting-started-guides/index.html). For example: _MyProject.Device_ (Class Library) and _MyProject.Device.App_ (nanoFramework Application).

**_MyProject.Device_**

Implement your logic here. You will be able to unit test this project (without hardware!). Place everything your software needs to do here, abstracting hardware-specific operations with interfaces. For example, if you want to blink a LED - create _IBlinker_ interface here with _void Blink(bool isOn);_ method.

**_MyProject.Device.App_**

This is the entry point to your software. Use _DeviceBuilder_ to link all components together (MAKO IoT and your code) in the _Main()_ method of _Program_ class. Also, implement your hardware-specific logic here. For example, concrete blinker class for the interface above: _LedBlinker : IBlinker_. Link the interface with the class in _ConfigureDI_ section of _DeviceBuilder_.

## Test your code
Create [nanoFramework test project](https://docs.nanoframework.net/content/unit-test/index.html) and implement unit tests for your logic from _MyProject.Device_ (Class Library).

## Give it a go!
Connect your device, Set Startup Project to _MyProject.Device.App_ (nanoFramework Application) and run it. 



Take a look at [Samples](https://github.com/CShark-Hub/Mako-IoT.Samples).

## MAKO IoT components

### Composition & Abstractions
- [Device](https://github.com/CShark-Hub/Mako-IoT.Device)
- [Interface](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Interface)
- [Dependency Injection](https://github.com/CShark-Hub/Mako-IoT.Device.Services.DependencyInjection)

### Network & Messaging
- [MQTT](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Mqtt)
- [Message Bus](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Messaging)
- [WiFi](https://github.com/CShark-Hub/Mako-IoT.Device.Services.WiFi)
- [API/Web Server](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Server)
- [WiFi AP](https://github.com/CShark-Hub/Mako-IoT.Device.Services.WiFi.AP)
- [Mediator](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Mediator)
- [Data Providers](https://github.com/CShark-Hub/Mako-IoT.Device.Services.DataProviders)
- [Data Contracts](https://github.com/CShark-Hub/Mako-IoT.Messages)

### Configuration
- [Configuration](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Configuration)
- [Configration Metadata](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Configuration.Metadata)
- [Configuration API](https://github.com/CShark-Hub/Mako-IoT.Device.Services.ConfigurationApi)
- [Configuration API Model](https://github.com/CShark-Hub/Mako-IoT.ConfigurationApi.Model)
- [Configuration Manager](https://github.com/CShark-Hub/Mako-IoT.Device.Services.ConfigurationManager)

### Storage
- [NVS](https://github.com/CShark-Hub/Mako-IoT.Device.Services.FileStorage)

### System Utils
- [Logging](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Logging)
- [Logs storage](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Logging.Storage)
- [Scheduler](https://github.com/CShark-Hub/Mako-IoT.Device.Services.Scheduler)
- [Invoker](https://github.com/CShark-Hub/Mako-IoT.Invoker)


### Displays & Hardware
- [Display Abstractions](https://github.com/CShark-Hub/Mako-IoT.Device.Displays.Core)
- [LED](https://github.com/CShark-Hub/Mako-IoT.Device.Displays.Led)
- [I2C Bus](https://github.com/CShark-Hub/Mako-IoT.Device.Buses.I2C)
- [SSD1306](https://github.com/CShark-Hub/Mako-IoT.Device.Displays.SSD1306)

### Utils
- [String](https://github.com/CShark-Hub/Mako-IoT.String)
- [Time Zones](https://github.com/CShark-Hub/Mako-IoT.TimeZones)
- [iCalendar](https://github.com/CShark-Hub/Mako-IoT.ICalParser)

### .NET Core Components
- [Interfaces](https://github.com/CShark-Hub/Mako-IoT.Core.Services.Interface)
- [MQTT](https://github.com/CShark-Hub/Mako-IoT.Core.Services.Mqtt)
- [Message Bus](https://github.com/CShark-Hub/Mako-IoT.Core.Services.Messaging)
- [Configuration App](https://github.com/CShark-Hub/Mako-IoT.Core.Configuration.App.Client)
- [Metadata Generator](https://github.com/CShark-Hub/Mako-IoT.Core.Configuration.MetadataGenerator)

## [Samples](https://github.com/CShark-Hub/Mako-IoT.Samples)
- [Messaging]()
- [Configuration API](https://github.com/CShark-Hub/Mako-IoT.Samples/tree/main/ConfigurationAPI)
- [Log Storage](https://github.com/CShark-Hub/Mako-IoT.Samples/tree/main/LogStorage)
- [Mediator](https://github.com/CShark-Hub/Mako-IoT.Samples/tree/main/Mediator)
- [Waste Bins Calendar (full product example)](https://github.com/CShark-Hub/Mako-IoT.Samples/tree/main/WasteBinsCalendar)

