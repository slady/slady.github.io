equivalent function for fmod() in Java

double fmod(double x, double y)
float fmodf(float x, float y)

The fmod functions compute the floating-point remainder of dividing x by y.

The return value is x - n y, where n is the quotient of x / y, rounded to the first integer towards zero.

Mindprod has a good overview of how modulus works in Java (look right at the end for floating point modulus).

http://mindprod.com/jgloss/modulus.html

Floating Point %
% is also defined to work with float and double operands, though that use is quite rare.

The result of a floating-point remainder operation as computed by the % operator is not the same as that produced by the remainder operation defined by the IEEE 754 floating point standard.
The IEEE (Institute of Electrical & Electronics Engineers) 754 remainder operation computes the remainder from a rounding division, not a truncating division.

% on floating-point operations behaves analogously to the integer remainder operator;
this may be compared with the C library function fmod.

The IEEE 754 remainder operation may be computed by the library routine Math. IEEEremainder.
(Note the violation of the naming conventions.)
