universal-panel-adapter
=======================

Using a cheap Arduino mini pro or nano this sketch allows you to interface a panel like Viki via SPI.

Specifically used for running I2C and parallel panels on a Smoothie compatible board.

Viki to Nano
---------------

	SDA -> A4
	SCL -> A5
	ENCA -> D2
	ENCB -> D3
	Gnd -> Gnd
	+5v -> +5v

Smoothie to Nano
----------------
	MOSI -> D11
	MISO -> D12
	SCK -> D13
	SS -> D10
	BUSY -> D4 (And set panel.busy_pin in config to a spare Smoothie pin)

Smoothie config
---------------

	panel.lcd                                   universal_adapter #
	panel.spi_channel                           0                 # spi channel to use (0- MISO 0.17, MOSI 0.18, SCK 0.15, SS 0.16)
	panel.spi_cs_pin                            0.16              # spi chip select
	panel.busy_pin                              2.13              # busy pin (Azteeg X5 use 2.11)

