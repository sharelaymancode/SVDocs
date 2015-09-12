# Randomize
1. Rand does not get a random value when an object is created. It only gets the rand value when object is randomized. The variable does not have randomize method.
Code|
-------------------------------|
program main;
  
  class topTestcase;
    rand bit[10:0] dude;
    function new();
    endfunction
  endclass
  //topTestcase test;
  initial begin
    topTestcase top =new();
    $display("Object -%d",top.dude);
    top.randomize();
    $display("Object- %d",top.dude);
  end

endprogram


module top;
  main tb();
  dut u_dut();
endmodule 

