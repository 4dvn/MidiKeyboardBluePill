# MidiKeyboardBluePill
This is software for the STM32F103 Microcontroller to convert serial midi into the outputs that would be generated by the Hybrid Music 4000 keyboard for the BBC Micro and BBC Master.

A BluePill board, plus optocoupler circuit is all that is required to get this to work. A complete hardware design will be forthcoming.

  Pins used: Userport PB0-7 (even pins 6-20) are on GPIOs PB4,6-12
  Userport CB1 (pin 2) -> Clk, GPIO PB13  (SPI2) - add external 10k pullup to 5V
  Userport CB2 (pin 4) -> MOSI, GPIO PB15 (SPI2)
  MIDI serial in (3.3V) -> GPIO PA3  (USART2)
  PA5 - Button (to ground) to program channel (press once and next note sets the channel, press twice and channel is ignored),
  PA4 - LED (active low, 560R to 3.3V) to indicate programming mode.
