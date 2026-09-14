`timescale 1ns / 1ps
//////////////////////////////////////////////////////////////////////////////////
// Company: 
// Engineer: 
// 
// Create Date: 08/06/2026 12:19:01 AM
// Design Name: 
// Module Name: APB#_decoder
// Project Name: 
// Target Devices: 
// Tool Versions: 
// Description: 
// 
// Dependencies: 
// 
// Revision:
// Revision 0.01 - File Created
// Additional Comments:
// 
//////////////////////////////////////////////////////////////////////////////////


module apb3_decoder(

    input  wire    psel,
    input  wire [7:0] paddr,

    output reg     uart_sel,
    output reg   gpio_sel,
    output reg  fifo_sel,
    output reg  pwm_sel

);

always @(*) begin

    uart_sel = 1'b0;
    gpio_sel = 1'b0;
    fifo_sel = 1'b0;
    pwm_sel  = 1'b0;

    if (psel) begin
        case (paddr)

            8'h05: uart_sel = 1'b1;  //0000_0101

            8'h10: gpio_sel = 1'b1;  // 0001_0000

            8'h20: fifo_sel = 1'b1;  // 0010_0000

            8'h30: pwm_sel  = 1'b1;   //0011_0000

            default: ;

        endcase
    end

end

endmodule
