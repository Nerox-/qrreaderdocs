<style>.codehilite{padding-top:2px;padding-bottom:6px;}</style>

__A Barcode/QR Reader for Corona SDK development.__

## Quick Start

When you build using the Corona Simulator, the server automatically takes care of integrating the plugin into your project.

All you need to do is add an entry into a plugins table of your __build.settings__. The following is an example of a build.settings file:

```lua
settings =
{
    plugins =
    {
        ["plugin.qrreader"] =
        {
            publisherId = "com.andrewwahid",
        },
    },      
}
```
Sample Project<br>
https://github.com/Nerox-/QRReader-Sample<br>

---

## API Directory

### QR Reader API

#### [startScan (params)](startScan.md)

### Events

#### [onScanComplete](onScanComplete.md)
