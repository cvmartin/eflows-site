
## A real-world approach: limiting power distribution though timeframes

Of the two approaches described above, the *timeframe* one is more elegant, but requires more data. Specifically, it requires to know the state of charge of the EV battery, as well as its total capacity and the deadlines when the energy shall be dispatched. In addition, it is important to know the rate at which the charging point can deliver power, and the rate at which the EV can assimilate it. 

In comparison, the *power distribution* approach just requires to decide few parameters, that do not even need to be associated with the EVs; they could instead depend on the user cards employed at charging poles. Hence, this alternative seems more ready for use it in a real-world scenario.

Still, some advantages can be taken from the *timeframe* approach. If the scale is large enough (district or city) and the flexible demand of EVs can be predicted, then `foreshift()` can be used to specify the volume of demand that shall be consumed in the next hours in order to optimize the grid usage. This volume of demand (plus perhaps a safety margin) is what is used in the *power distribution* approach as grid capacity. Instead of using the "real" one, an "artificial" grid capacity can be defined to achieve certain objectives; for instance charge EVs later in the day, when more renewable energy will be available. 

In a minimum viable case, the parameters of `share` and `level` could be the same for each EV, meaning the available grid capacity will be exchanged equally among the EVs. With a bit more engineering, a better option could be to modify these parameters over time, so the EVs that started to charge earlier can have access to more power share if their session is not finished yet. 

