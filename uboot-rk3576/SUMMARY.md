# U-Boot RK3576 upstream snapshot

Source: `u-boot/u-boot` `master`
Output root: `./uboot-rk3576`

## Complete list of files saved
- `arch/arm/mach-rockchip/rk3576/Kconfig`
- `arch/arm/mach-rockchip/rk3576/MAINTAINERS`
- `arch/arm/mach-rockchip/rk3576/Makefile`
- `arch/arm/mach-rockchip/rk3576/clk_rk3576.c`
- `arch/arm/mach-rockchip/rk3576/rk3576.c`
- `arch/arm/mach-rockchip/rk3576/syscon_rk3576.c`
- `configs/generic-rk3576_defconfig`
- `configs/nanopi-m5-rk3576_defconfig`
- `configs/omni3576-rk3576_defconfig`
- `configs/roc-pc-rk3576_defconfig`
- `configs/rock-4d-rk3576_defconfig`
- `configs/sige5-rk3576_defconfig`
- `drivers/clk/rockchip/clk_rk3576.c`
- `drivers/pinctrl/rockchip/pinctrl-rk3576.c`
- `drivers/ram/rockchip/sdram_rk3576.c`
- `drivers/reset/rst-rk3576.c`
- `dt-bindings/clock/rockchip,rk3576-cru.h`
- `dt-bindings/power/rockchip,rk3576-power.h`
- `dt-bindings/reset/rockchip,rk3576-cru.h`
- `dts/upstream/src/arm64/rockchip/rk3576-100ask-dshanpi-a1.dts`
- `dts/upstream/src/arm64/rockchip/rk3576-pinctrl.dtsi`
- `dts/upstream/src/arm64/rockchip/rk3576.dtsi`

## Requested files not present at HEAD/master
- `include/configs/rk3576.h` — not present in `u-boot/u-boot` `master`
- `configs/dshanpi-a1-rk3576_defconfig` — not present in `u-boot/u-boot` `master`
- `dts/upstream/src/arm64/rockchip/Makefile` — not present in `u-boot/u-boot` `master`

## RK3576 defconfigs found at HEAD/master
- `generic-rk3576_defconfig`
- `nanopi-m5-rk3576_defconfig`
- `omni3576-rk3576_defconfig`
- `roc-pc-rk3576_defconfig`
- `rock-4d-rk3576_defconfig`
- `sige5-rk3576_defconfig`

## Exact rk3576-related lines from requested Makefile/Kconfig files

### `arch/arm/mach-rockchip/Kconfig`
```text
config ROCKCHIP_RK3576
bool "Support Rockchip RK3576"
select ARM64
select SUPPORT_SPL
select SPL
select CLK
select PINCTRL
select RAM
select REGMAP
select SYSCON
select BOARD_LATE_INIT
select DM_REGULATOR_FIXED
select DM_RESET
imply ARMV8_CRYPTO
imply ARMV8_SET_SMPEN
imply BOOTSTD_FULL
imply DM_RNG
imply FIT
imply LEGACY_IMAGE_FORMAT
imply MISC
imply MISC_INIT_R
imply MMC_HS200_SUPPORT if MMC_SDHCI_ROCKCHIP
imply OF_LIBFDT_OVERLAY
imply OF_LIVE
imply OF_UPSTREAM
imply PHY_GIGE if DWC_ETH_QOS_ROCKCHIP
imply RNG_ROCKCHIP
imply ROCKCHIP_COMMON_BOARD
imply ROCKCHIP_COMMON_STACK_ADDR
imply ROCKCHIP_EXTERNAL_TPL
imply ROCKCHIP_OTP
imply SPL_ATF
imply SPL_ATF_NO_PLATFORM_PARAM if SPL_ATF
imply SPL_CLK
imply SPL_DM_SEQ_ALIAS
imply SPL_FIT_SIGNATURE
imply SPL_LOAD_FIT
imply SPL_MMC_HS200_SUPPORT if SPL_MMC && MMC_HS200_SUPPORT
imply SPL_OF_CONTROL
imply SPL_PINCTRL
imply SPL_RAM
imply SPL_REGMAP
imply SPL_SERIAL
imply SPL_SYSCON
imply ENV_RELOC_GD_ENV_ADDR
imply SYSRESET
help
  The Rockchip RK3576 is a ARM-based SoC with quad-core Cortex-A72 and
  and quad-core Cortex-A53.

source "arch/arm/mach-rockchip/rk3576/Kconfig"
default 0x40000000 if ROCKCHIP_RK3576
```

### `arch/arm/mach-rockchip/Makefile`
```text
obj-$(CONFIG_ROCKCHIP_RK3576) += rk3576/
```

### `drivers/clk/rockchip/Makefile`
```text
obj-$(CONFIG_ROCKCHIP_RK3576) += clk_rk3576.o
```

### `drivers/ram/rockchip/Makefile`
```text
obj-$(CONFIG_ROCKCHIP_RK3576) += sdram_rk3576.o
```

### `drivers/pinctrl/rockchip/Makefile`
```text
obj-$(CONFIG_ROCKCHIP_RK3576) += pinctrl-rk3576.o
```

### `dts/upstream/src/arm64/rockchip/Makefile`
```text
(not present at HEAD/master)
```

### Relevant DTS build list file checked: `arch/arm/dts/Makefile`
```text
(no rk3576-related lines at HEAD/master)
```

## `arch/arm/Kconfig`
```text
No CONFIG_ROCKCHIP_RK3576 block is present in arch/arm/Kconfig at HEAD/master.
RK3576 is defined in arch/arm/mach-rockchip/Kconfig instead.
```

## Additional notes
- The local output path is `./uboot-rk3576` because writing outside the repository was restricted in this environment.
- `rk3576-pinctrl.dtsi` is large and was preserved as fetched.
