ccflags-y += -I$(src)
ifeq ($(CONFIG_BACKPORT_INTEGRATE),)
obj-m += compat.o
else
obj-y += compat.o
endif
compat-y += main.o

# Kernel backport compatibility code
compat-$(CPTCFG_KERNEL_3_0) += compat-3.0.o
compat-$(CPTCFG_KERNEL_3_1) += compat-3.1.o
compat-$(CPTCFG_KERNEL_3_2) += backport-3.2.o
compat-$(CPTCFG_KERNEL_3_3) += compat-3.3.o
compat-$(CPTCFG_KERNEL_3_4) += compat-3.4.o
compat-$(CPTCFG_KERNEL_3_5) += compat-3.5.o user_namespace.o
compat-$(CPTCFG_KERNEL_3_6) += compat-3.6.o
compat-$(CPTCFG_KERNEL_3_7) += compat-3.7.o
compat-$(CPTCFG_KERNEL_3_8) += compat-3.8.o
compat-$(CPTCFG_KERNEL_3_9) += compat-3.9.o
ifneq ($(CPTCFG_REGMAP),)
ifeq ($(CPTCFG_LZO_COMPRESS),)
compat-$(CPTCFG_KERNEL_3_9) += regmap/lzo1x_compress.o
endif
ifeq ($(CPTCFG_LZO_DECOMPRESS),)
compat-$(CPTCFG_KERNEL_3_9) += regmap/lzo1x_decompress_safe.o
endif
endif
compat-$(CPTCFG_KERNEL_3_9) += clk/clk-devres.o clk/clkdev.o clk/clk.o clk/clk-divider.o
compat-$(CPTCFG_KERNEL_3_9) += clk/clk-fixed-factor.o clk/clk-fixed-rate.o clk/clk-gate.o clk/clk-mux.o
ifeq  ($(CONFIG_I2C),)
ifneq ($(CPTCFG_REGMAP_I2C),)
ifneq ($(CPTCFG_I2C_BOARDINFO),)
compat-$(CPTCFG_KERNEL_3_9) += i2c/i2c-boardinfo.o
endif
compat-$(CPTCFG_KERNEL_3_9) += i2c/i2c-core.o i2c/i2c-dev.o i2c/i2c-mux.o
endif
endif
ifeq ($(CPTCFG_FW_LOADER_USER_HELPER),)
compat-$(CPTCFG_KERNEL_3_9) += base/firmware_class.o
endif
compat-$(CPTCFG_KERNEL_3_10) += backport-3.10.o
compat-$(CPTCFG_KERNEL_3_12) += backport-3.12.o
compat-$(CPTCFG_KERNEL_3_13) += backport-3.13.o
compat-$(CPTCFG_KERNEL_3_14) += backport-3.14.o
compat-$(CPTCFG_KERNEL_3_15) += backport-3.15.o
compat-$(CPTCFG_KERNEL_3_17) += backport-3.17.o
compat-$(CPTCFG_KERNEL_3_18) += backport-3.18.o
compat-$(CPTCFG_KERNEL_3_19) += backport-3.19.o
compat-$(CPTCFG_KERNEL_4_0) += backport-4.0.o
compat-$(CPTCFG_KERNEL_4_1) += backport-4.1.o
compat-$(CPTCFG_KERNEL_4_2) += backport-4.2.o
compat-$(CPTCFG_KERNEL_4_3) += backport-4.3.o
compat-$(CPTCFG_KERNEL_4_4) += backport-4.4.o

compat-$(CPTCFG_BPAUTO_BUILD_CRYPTO_CCM) += crypto-ccm.o
#compat-$(CPTCFG_BPAUTO_BUILD_DMA_SHARED_HELPERS) += dma-shared-helpers.o
compat-$(CPTCFG_BPAUTO_BUILD_DMA_SHARED_HELPERS) += base/dma-buf.o
compat-$(CPTCFG_BPAUTO_BUILD_WANT_DEV_COREDUMP) += drivers-base-devcoredump.o
compat-$(CPTCFG_BPAUTO_RHASHTABLE) += lib-rhashtable.o
cordic-objs += lib-cordic.o
obj-$(CPTCFG_BPAUTO_BUILD_CORDIC) += cordic.o
compat-$(CPTCFG_BPAUTO_BUILD_CRYPTO_CCM) += crypto-ccm.o
compat-$(CPTCFG_BPAUTO_BUILD_FRAME_VECTOR) += mm-frame_vector.o
compat-$(CPTCFG_BPAUTO_BUILD_HDMI) += drivers-video-hdmi.o
compat-$(CPTCFG_REGMAP) += regmap/regmap.o regmap/regcache.o
compat-$(CPTCFG_REGMAP) += regmap/regcache-rbtree.o regmap/regcache-lzo.o regmap/regcache-flat.o
compat-$(CPTCFG_REGMAP_I2C) += regmap/regmap-i2c.o
