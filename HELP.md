# mktgen() function for calculating mean kinetic temperature

## Description

The mean kinetic temperature (MKT) of a time series of temperature readings, which may be unequally spaced in time, and have duplicate time readings, is calculated in two different ways.  One way follows the method of Tong & Lock (2015) and the other follows a formula found on the wikipedia page for mean kinetic temperature.

## Usage

mktgen(timevec,tempvec, ea)

## Arguments

timevec is a chron object representing a series of time points.

tempvec is a numeric vector of temperature readings in degrees Celsius.

ea is a scalar, equal to the heat of activation for the degradation reaction, in units of kJ.  The default value is 83.144 kJ.

## Details

timevec and tempvec must be of the same length.  The function will compare the lengths, but will not gracefully produce an error message if the lengths don't match.

More generally, the function does not check for or correct for inappropriate inputs, so the user should take care to prepare the inputs as expected.

If there are duplicate time readings, these are compressed into a single reading, and the corresponding temperature is the arithmetic average of the duplicates for that time.  This is done prior to calculating MKT.

The mktgen() function outputs a list of two values.  The first, mkt1, is the mean kinetic temperature using the method of Tong & Lock (2015), which uses the trapezoidal rule to estimate Area Under the Curve (AUC).  The second, mkt2, is the mean kinetic temperature using the formula found on the wikipedia page, https://en.wikipedia.org/wiki/Mean_kinetic_temperature.  In both cases, the units are in Celsius degrees.

## Author(s)

Christopher Tong

## Reference

C. Tong & A. Lock, 2015:  A computational procedure for mean kinetic temperature using unequally spaced data.  Joint Statistical Meetings, Biopharmaceutical Section, 2065-2070.

## Example

To be added later.
