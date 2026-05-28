# projekt_nmo
### class Intersection
Konstruktor:
* green_light - długość zielonego N-S
* red_light - długość zielonego N-S
* yellow_light - długość żółtego - ruch ustaje
* capacity_ver, capacity_hor - przepustowość skrzyżowania N-S i E-W
* offset - przesunięcie względem całego cyklu - wartość [0.0; 1.0]

step - jedna sekunda (tick) symulacji skrzyżowania

return outputs - zwraca słownik {'queue_time_sum': 0, 'output_N': 0, 'output_S': 0, 'output_W': 0, 'output_E': 0, 'state': 0} ,gdzie:
* queue_time_sum - suma wszystkich samochodów stojących w kolejkach
* outputs_(N/S/W/E) - ile samochodów wyjeżdża w każdym kierunku ze skrzyżowania
* state - stan świateł na skrzyżowaniu

### simulation
params - wektor wygenerowany przez algorytm metaheurystyczny składający się z wartości: (green_light, red_light, offset) * ilość skrzyżowań (w naszym modelu 4 - A, B, C, D)
> należy pamiętać, że wartość offset przyjmuje wartości od 0.0 do 1.0

connections - słownik definiujący połączenia między skrzyżowaniami

traffic_map - bazowe natężenie ruchu na skrzyżowaniach

return cost - **wartość minimalizowana**

