# Yunit #

```java
assertEquals(1000, METRE.to(MILLI))                                        // Convert 1 metre to millimetres
assertEquals(2, measure(20, MILLI).to(CENTI))                              // Convert 20 millimetres to centimetres
assertEquals(5, measure(3, METRE).map(i -> i + 2).to(METRE))               // Add 2 metres to 3 metres to get 5 metres
assertEquals(6, measure(300, CENTI).multiply(measure(2, METRE)).to(METRE)) // Multiply 300 centimetres by 2 metres to get 6 metres squared
assertEquals(1, area(10_000, CENTI).to(METRE))                             // Get 10,000 cm squared in m squared
assertEquals(40_000, measure(2, METRE).square().to(CENTI))                 // Create a square with 2m sides and get the area in centimetres
assertEquals(1_000_000, METRE.lift(3).to(CENTI))                           // "Lift" 1m to 1m^3 then get this volume in cm^3
```