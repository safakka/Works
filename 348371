--------348371-ŞAFAK KİBAR------------




library IEEE;
use IEEE.STD_LOGIC_1164.ALL;
use IEEE.STD_LOGIC_ARITH.ALL;
use IEEE.STD_LOGIC_UNSIGNED.ALL;

entity EightBitHalfAdder is
  port ( A : in std_logic_vector(7 downto 0);
         B : in std_logic_vector(7 downto 0);
         S : out std_logic_vector(7 downto 0);
         Carry: out std_logic );

end EightBitHalfAdder ;
architecture Behavioral of EightBitHalfAdder is
  signal Cout : std_logic_vector (14 downto 0):="00000000000000";
  signal Sara : std_logic_vector (6 downto 0):="000000";
  signal Orr : std_logic_vector (5 downto 0 ):="00000";
begin

  S(0)<=A(0) xor B(0);
  Sara(0)<=A(1) xor B(1);
  Sara(1)<=A(2) xor B(2);
  Sara(2)<=A(3) xor B(3);
  Sara(3)<=A(4) xor B(4);
  Sara(4)<=A(5) xor B(5);
  Sara(5)<=A(6) xor B(6);
  Sara(6)<=A(7) xor B(7);
  Cout(0)<=A(0) and B(0);
  Cout(1)<=A(1) and B(1);
  Cout(2)<=A(2) and B(2);
  Cout(3)<=A(3) and B(3);
  Cout(4)<=A(4) and B(4);
  Cout(5)<=A(5) and B(5);
  Cout(6)<=A(6) and B(6);
  Cout(7)<=Sara(0) and Cout(0);
  Orr(0)<=Cout(1) or Cout(7);
  Cout(8)<=Sara(1) and Orr(0);
  Orr(1)<=Cout(2) or Cout(8);
  Cout(9)<=Sara(2) and Orr(1);
  Orr(2)<=Cout(3) or Cout(9);
  Cout(10)<=Sara(3) and Orr(2);
  Orr(3)<=Cout(4) or Cout(10);
  Cout(11)<=Sara(4) and Orr(3);
  Orr(4)<=Cout(5) or Cout(11);
  Cout(12)<=Sara(5) and Orr(4);
  Orr(5)<=Cout(6) or Cout(12);
  Cout(13)<=Sara(6) and Orr(5);
  Carry<=Cout(13) or Cout(14);

  end Behavioral;
  
