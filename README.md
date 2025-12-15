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

