So, I got a clone R36S and, it was alright was working fine - until I noticed I was not able to connect to the internet. Not with WIFI dongle nor with USB tether from my phone. - The stock rom was ArkOS 2.0 maybe from August 2024, with linux kernel 5.10 (5 is confirmed - rest I forgot).
Them I flashed arkos4clone https://github.com/lcdyk0517/arkos4clone and chose the K36 DTB files. It worked fine, and the USB tether was working perfectly.

One, important thing though - the LEDs, they were not working as expected, my blue and red light was completely off. Even when charging. I then de-compiled the rk3326-k36-linux.dtb and found out this dtb actually had wrong LED addresses and configuration. Then I did same with the rf3536k3ka.dts and found out the correct LED addresses and configuration. Then I patched out the rk3326-k36-linux.dtb - now everything works, the LED works as well, plus I got internet access. Check out the DTS Files on my github:
https://github.com/immo2n/R36S-K36-DTB-PATCH


# Rockchip DTS Files

Device tree source files for Rockchip RK3326-based game console.

## Boot Logo Requirements

The boot logo (`logo.bmp`) must be:
- **24-bit RGB color depth** (NOT 8-bit indexed)
- **640 x 480 pixels**
- **Uncompressed BMP format**
- File size: ~900KB

The working logo is 24-bit RGB. 8-bit indexed color BMP files will not display.

## Files

- `rk3326-k36-linux-patch.dts` - Main device tree source
- `rk3326-k36-linux.dtb` - Compiled device tree binary

