---
-api-id: T:Windows.ApplicationModel.Background.DeviceUseTrigger
-api-type: winrt class
---

<!-- Class syntax.
public class DeviceUseTrigger : Windows.ApplicationModel.Background.IBackgroundTrigger, Windows.ApplicationModel.Background.IDeviceUseTrigger
-->

# Windows.ApplicationModel.Background.DeviceUseTrigger

## -description
Represents an event that a Windows Runtime app can trigger to initiate a long-running operation with a device or sensor.

**DeviceUseTrigger** lets your Windows Runtime app access sensors and peripheral devices in the background, even when your foreground app is suspended. For example, depending on where your app is running, it could use a background task to synchronize data with devices or monitor sensors.

This class can be used in UWP app and Windows Phone 8.x app. However, a **DeviceUseTrigger** background task supports different APIs, and is subject to different policies, depending where it's running (PC or phone). To learn more about these differences, see [Accessing sensors and devices from a background task](http://msdn.microsoft.com/library/ccde8565-8dae-44fc-aded-3a0fee759930).

> [!IMPORTANT]
> This trigger cannot be used with single-process background tasks.

For a sample that shows how to use **DeviceUseTrigger** on a PC, see the [Custom USB device sample](http://go.microsoft.com/fwlink/p/?LinkId=301975 ). For a phone sample, see the [Background Sensors sample](http://go.microsoft.com/fwlink/p/?LinkId=393307).

## -remarks
For more about policy requirements, see [Accessing sensors and devices from a background task](http://msdn.microsoft.com/library/ccde8565-8dae-44fc-aded-3a0fee759930)

> Before your app triggers a background task on a phone, it must first call [BackgroundExecutionManager.RequestAccessAsync](https://docs.microsoft.com/uwp/api/windows.applicationmodel.background.backgroundexecutionmanager#Windows_ApplicationModel_Background_BackgroundExecutionManager_RequestAccessAsync) to check if the app is able to request a background task. This check is not required when your app is running on a PC.

## -examples

## -see-also
[IBackgroundTrigger](ibackgroundtrigger.md)
