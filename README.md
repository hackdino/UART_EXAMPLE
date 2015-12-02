# Uart_Example
## UART usage with uc/OS-3 from Micrium.

## Hardware => XMC4500 Relax Kit from Infineon.

Look at the following files!

    ..* COM-Task in app.c
    
    ..* BSP_IntHandler_Uart_Recive in bsp_init.c
    
    ..* BSP_UART_Init in bsp_uart.c
    
Was developed by hackdino according to the following pattern:

    [a link](https://doc.micrium.com/display/osiiidoc/Keeping+the+Data+in+Scope)
    
Usage:
    PIN_Layout: RXD = P0.0  TXD = P0.1 Mode: 8N1 9600
    Start Byte => 0x1  Stop Byte => 0x17
    
    Example: 
      Input:   0x1   0x46   0x48  0x54  0x57  0x17        # Send from Terminal
  		  		| Start | "F" | "H" | "T" | "W" | Stop |
  		Output:                                             # Print in COM-Task
  		    Message : FHTW
  		    Lenght: 4
  		    
  
