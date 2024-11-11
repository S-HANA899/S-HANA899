module risc_v_tb();
    reg clk;
    reg [3:0]a,b,op;
    wire[7:0]y;
risc_v  dut(
.clk(clk),
.a(a),
.b(b),
.op(op),
.y(y));
initial begin
clk=0;
forever #5 clk=~clk;
end
initial begin
#30
a=0;
b=0;
op=0;
#10
a=2;
b=5;
op=23;
#10
a=5;
b=5;
op=23;
#10
end
endmodule
