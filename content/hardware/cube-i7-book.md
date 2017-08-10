---
Title: Cube i7 Book
show_in_header_nav: false
---

*&larr; back to [Hardware](?hardware)*

# Cube i7 Book

Nifty little 10.6-inch Core M3-6Y30 tablet PC with compatible Wacom stylus. See [techtablets.com review](https://techtablets.com/cube-i7-book/review/).

## Naming quirks explained

- Yes, the vendor is actually called Cube
    - Legally, the [Shenzhen Alldo Cube Technology and Science Co., Ltd](http://www.51cube.com/en/About.asp?ID=1)
    - In Chinese, 「酷比魔方」 (this is what you see in the BIOS/EFI boot screen)
- Yes, the model is actually "i7" even though the processor is not, in fact, an Intel Core i7, but instead, an Intel Core m3

## Procurement

- As with many Chinese devices, [GearBest](www.gearbest.com/tablet-pcs/pp_366651.html) is probably your best bet.
- Shape and size doesn't suit many tablet cases - in Sydney, the best option I've found is [Cleanskin Universal 9-10" Tablet Case Black via OfficeWorks](https://www.officeworks.com.au/shop/officeworks/p/cleanskin-universal-9-10-tablet-case-black-fcul988bla).

## Hardware

- WiFi can be a bit slow but generally reliable
- Bluetooth seems to work fine
- Comes with a super-funky microUSB 3.0/SS to female USB adapter, but no, this doesn't charge the tablet 
- Comes with a [FJ-SW1202000C](https://www.google.com.au/search?q="FJ-SW1202000C") charger with 24W (12V 2A) output
- USB-C port successfully charges the tablet - use the [Apple 29W USB-C Power Adapter](https://www.apple.com/au/shop/product/MJ262X/A/apple-29w-usb-c-power-adapter).
- USB-C port works fine with Apple's [VGA Multiport Adapter](https://www.apple.com/au/shop/product/MJ1L2AM/A/usb-c-vga-multiport-adapter) and [Digital AV (HDMI) Multiport Adapter](https://www.apple.com/au/shop/product/MJ1K2AM/A/usb-c-digital-av-multiport-adapter).

## Linux

- Works pretty well with Linux (tested 2016~2017 with Arch Linux)
- microSD slot works fine
- No palm rejection - use `xinput` to disable the touchscreen so you can use pen only
- No accelerometer support for auto-rotate - you'll need to use some shell scripts

## Drivers

Poorly documented by the vendor so here we go:

- Wacom FEEL driver