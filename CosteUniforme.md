# Algoritmo de búsqueda por coste uniforme
Prioridades:
1. Menor coste
2. FIFO
## Nomenclatura
N (np) $^{g}$

N = nodo

np = nodo padre

g = coste ( g' + c )

## Ejercicio
F = { **Ou $^{0}$** } → Test( Ou $^{0}$ ) → C = { Ou $^{0}$ }

F = { **Po (Ou) $^{175}$**, Be (Ou) $^{236}$ } → Test( Po (Ou) $^{175}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$ }

F = { **Be (Ou) $^{236}$**, Le (Po) $^{288}$, Be (Po) $^{300}$ } → Test( Be (Ou) $^{236}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$ }

F = { **Le (Po) $^{288}$**, Le (Be) $^{311}$, Pa (Be) $^{348}$, Va (Be) $^{348}$ } → Test( Le (Po) $^{288}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$ }

F = { **Pa (Be) $^{348}$**, Va (Be) $^{348}$, Oso (Le) $^{409}$, Pa (Le) $^{419}$ } → Test( Pa (Be) $^{348}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$ }

F = { **Va (Be) $^{348}$**, Oso (Le) $^{409}$, Bu (Pa) $^{441}$ } → Test( Va (Be) $^{348}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$ }

F = { **Oso (Le) $^{409}$**, Bu (Pa) $^{441}$, Ar (Va) $^{443}$ } → Test( Oso (Le) $^{409}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$ }

F = { **Bu (Pa) $^{441}$**, Ar (Va) $^{443}$, Bu (Oso) $^{468}$ } → Test( Bu (Pa) $^{441}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$ }

F = { **Ar (Va) $^{443}$**, Lo (Bu) $^{591}$, So (Bu) $^{584}$ } → Test( Ar (Va) $^{443}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$ }

F = { Lo (Bu) $^{591}$, So (Bu) $^{584}$, **Os (Ar) $^{501}$** } → Test( Os (Ar) $^{501}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$ }

F = { Lo (Bu) $^{591}$, **So (Bu) $^{584}$**, So (Os) $^{559}$, Ca (Os) $^{641}$ } → Test( So (Bu) $^{584}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$, So (Bu) $^{584}$ }

F = { **Lo (Bu) $^{591}$**, Ca (Os) $^{641}$, Ca (So) $^{650}$ } → Test( Lo (Bu) $^{591}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$, So (Bu) $^{584}$, Lo (Bu) $^{591}$ }

F = { **Ca (Os) $^{641}$**, Ca (Os) $^{641}$ } → Test( Ca (Os) $^{641}$ ) → C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$, So (Bu) $^{584}$, Lo (Bu) $^{591}$, Ca (Os) $^{641}$ }

## Resultado
C = { Ou $^{0}$, Po (Ou) $^{175}$, Be (Ou) $^{236}$, Le (Po) $^{288}$, Pa (Be) $^{348}$, Va (Be) $^{348}$, Oso (Le) $^{409}$, Bu (Pa) $^{441}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$, So (Bu) $^{584}$, Lo (Bu) $^{591}$, Ca (Os) $^{641}$ }

F = { Ca (Os) $^{641}$ }

Solución = { Ou $^{0}$, Be (Ou) $^{236}$, Va (Be) $^{348}$, Ar (Va) $^{443}$, Os (Ar) $^{501}$, Ca (Os) $^{641}$ }
