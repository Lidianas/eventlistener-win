# Event listener for Windows

**Usage:**

```
#include <QCoreApplication>
#include <wineventlistener.h>
#include <QList>
#include <QString>
int main(int argc, char *argv[])
{
    //Create a WinEventListener
    WinEventListener w;

    //Events to watch
    QList<QString> q{
        "UIA_ToolTipOpenedEventId",
        "UIA_ToolTipClosedEventId"
    };

    //Add events that you wanna watch to your listener
    w.addEventsToIdentify(q);

    //And.. have fun!
    w.listenerStart();

    QCoreApplication a(argc, argv);
    return a.exec();
}
```

With this library you should be able to capture all Microsoft UIAutomation events present here:
```
MontorableUIAutoEvents.h
```

This readme will be written one day.