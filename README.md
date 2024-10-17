# Descrierea proiectului:
SnakeGame este o recreare a celebrului joc retro "Snake", în care jucătorul controlează un șarpe pe o suprafață delimitată. Obiectivul principal al jocului este ca șarpele să consume "mere" (sau alte obiecte) care apar aleatoriu pe terenul de joc. După fiecare măr consumat, șarpele crește în dimensiune. Pe măsură ce șarpele se lungește, nivelul de dificultate crește, deoarece jucătorul trebuie să evite coliziunile cu pereții sau cu corpul șarpelui. Jocul se încheie atunci când șarpele se lovește de o margine sau de propriul corp.

Descrierea fișierelor:
point.hpp:
Rol: Definește structura Point, care reprezintă un punct în spațiul bidimensional, având coordonatele x și y. Acesta este folosit pentru a indica locația șarpelui, a mărului sau a altor obiecte de pe tabla de joc.

Structura Point:

Descriere: Reprezintă un set de coordonate (x, y) în spațiul bidimensional al jocului.
Constructor implicit: Inițializează coordonatele x și y la valoarea 0.
Constructor cu parametri: Permite inițializarea unui punct cu coordonate specifice pentru x și y.
snake.hpp:
Rol: Reprezintă șarpele și comportamentul acestuia pe parcursul jocului. Gestionarea segmentelor șarpelui și mișcările sale sunt incluse aici. De asemenea, acest fișier se ocupă de creșterea șarpelui atunci când acesta mănâncă și de detectarea eventualelor coliziuni.

Clasa Snake:

Descriere: Oferă mecanismele pentru mișcarea și gestionarea segmentelor corpului șarpelui.
segments[100]: Un array format din 100 de segmente, fiecare fiind un obiect de tip Point. Aceste segmente marchează pozițiile ocupate de șarpe pe terenul de joc.
length: Reține lungimea curentă a șarpelui, adică numărul de segmente active.
Constructor: Creează un șarpe cu un singur segment, inițial plasat la o locație prestabilită, cum ar fi coordonatele (10, 10).
Move(Point direction): Mută șarpele într-o anumită direcție (stânga, dreapta, sus, jos), actualizând pozițiile segmentelor astfel încât capul să se miște în direcția dorită, iar celelalte segmente să-l urmeze.
Grow(): Adaugă un segment suplimentar la coada șarpelui, bazat pe ultima poziție cunoscută a cozii.
GetHeadPosition(): Returnează poziția capului șarpelui, care este primul segment din array-ul segments.
board.hpp:
Rol: Reprezintă terenul de joc, unde șarpele se deplasează și unde apar merele. Gestionarea dimensiunii terenului și afișarea obiectelor pe acesta, inclusiv șarpele și merele, sunt controlate prin acest fișier.

Clasa Board:

Descriere: Definirea suprafeței de joc unde are loc acțiunea.
width și height: Variabile care definesc lățimea și înălțimea terenului de joc.
Constructor: Creează o tablă de joc cu dimensiunile specificate, cum ar fi o suprafață de 20x20 sau alte dimensiuni predefinite de utilizator.
GetWidth(): Returnează lățimea suprafeței de joc, utilă pentru a determina limitele laterale ale terenului.
GetHeight(): Returnează înălțimea suprafeței de joc, necesară pentru a verifica limitele superioare și inferioare.
Aceste fișiere colaborează pentru a oferi funcționalitatea completă a jocului Snake, permițând jucătorului să controleze șarpele și să navigheze prin provocările jocului.
