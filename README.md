# Selenium.WebDriver.Extensions
This library intends to provide useful object extensions to Selenium's .NET bindings.

At this moment it contains:

* Support for HTML5 Drag and Drop

This package is on NuGet: 

## Add to your project
Simply add a new NuGet dependency:

	Install-Package Selenium.WebDriver.Extensions

## Using
### HTML5 Drag and Drop

This feature depends on:

	https://github.com/Photonios/js-drag-and-drop-simulator

(It is included in this project, no need to do anything with it).

#### Example usage

The extension is on `IWebElement`:

	using OpenQA.Selenium.Extensions;

	IWebElement sourceElement = ...
	IWebElement targetElement = ...

	sourceElement.DragTo(targetElement);

In case you are using `EventFiringWebDriver` or anything else where your elements aren't actually `IWebElement` instances, you can manually specify the driver:

	sourceElement.DragTo(targetElement, this.Driver);