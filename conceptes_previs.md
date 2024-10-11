---
marp: true
style: pre.mermaid { all: unset; }
---
<!--
theme: gaia
size: 16:9
_class: lead
paginate: true
marp: false
backgroundColor: #000
backgroundImage: url('img/bg_ies.png')
-->
<style>
section::after {
  content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);}
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
table {
  margin-left: auto;
  margin-right: auto;
}
footer {
  font-size: 20px;
 }
header {
  font-size: 16px;
 }
</style>
<style scoped>
section {
  @extend .markdown-body;
  font-size: 28px;
  justify-content: top;
 }
</style>
# Conceptes Previs: Models d'Intel·ligència Artificial
#### Models d'Intel·ligència Artificial

## Conceptes previs

- Per a poder afrontar els temes relacionats amb búsquedes necessitarem alguns conceptes previs.
- En aquesta unitat ens centrarem en assolir-los.
- Els conceptes que necessitarem són:
  - Grafs
  - Arbres
  - Llistes i cues
  - Algorismes sobre grafs i arbres
  - Complexitat temporal i espacial

---

## Grafs

- **Teoria de Grafs**: La teoria de grafs és una branca de les matemàtiques que estudia les relacions entre objectes.
- Un graf és un conjunt de punts (nodes) connectats per línies (arestes).
- Molts problemes es poden representar com a grafs o xarxes:

  - **Transport**: carreteres, vies de tren, etc.
  - **Comunicacions**: xarxes informàtiques, xarxes socials.
  - **Distribució**: xarxes elèctriques, d'aigua, etc.
  - **Relacions**: relacions entre persones o conceptes.
  - **Dependències**: dependències entre tasques o processos.

---

## Història: Els ponts de Königsberg

- Els grafs van ser introduïts per **Leonhard Euler** al segle XVIII per resoldre el problema dels ponts de Königsberg.
- Euler va demostrar que no existia cap camí que passés per tots els ponts de la ciutat sense repetir cap pont més d'una vegada.
- Això va introduir el concepte de **graf eulerià**.

---

## Definicions bàsiques de Grafs

- Un graf pot ser:
  - **Pesat**: Si les arestes tenen un pes.
  - **Cíclic**: Si conté cicles (un camí que comença i acaba en el mateix node).
  - **Dirigit**: Si les arestes tenen direcció.
  - **Acíclic dirigit (DAG)**: Utilitzat freqüentment en programació.
  - **Complet**: Tots els nodes estan connectats entre si.
  - **Connex**: Existeix un camí entre qualsevol parell de nodes.

---

## Estructures de dades per a representar Grafs

1. **Matriu d'adjacència**:
   - Una matriu quadrada on files i columnes representen nodes del graf.
   - Si hi ha una aresta, el valor és 1, en cas contrari 0.
   - Adequada per a grafs densos.

2. **Llista d'adjacència**:
   - Una llista de llistes o diccionari que conté nodes adjacents.
   - Generalment més eficient en espai que la matriu d'adjacència.

---

## Tipus de problemes en grafs

- **Recorregut**: Trobar un camí entre dos nodes.
- **Connexió**: Saber si dos nodes estan connectats.
- **Cicles**: Trobar si el graf té cicles.
- **Camí mínim**: Trobar el camí de cost mínim.
- **Flux màxim**: Trobar el flux màxim entre dos nodes.

---

## Algorismes importants sobre Grafs

- **Recorregut en amplada (BFS)**.
- **Recorregut en profunditat (DFS)**.
- **Algorisme de Dijkstra**.
- **Algorisme de Prim**.
- **Algorisme de Kruskal**.
- **Algorisme de Bellman-Ford**.
- **Algorisme de Ford-Fulkerson**.

---

## Arbres

- **Definició**: Un arbre és un graf connex, acíclic i no dirigit.
- Els arbres són utilitzats per representar jerarquies (sistemes de fitxers, sintaxi de llenguatges, etc.).

---

## Tipus d'arbres

- **Arbre general**: Cada node pot tenir un nombre arbitrari de fills.
- **Arbre binari**: Cada node pot tenir com a màxim dos fills.
- **Arbre binari de cerca**: Els nodes a l'esquerra són menors i els de la dreta són majors.

---

## Llistes, cues i piles

1. **Llista enllaçada**:
   - Estructura de dades on cada element conté un punter al següent.

2. **Cua**:
   - Estructura FIFO (First In First Out), on els elements s'afegeixen per un extrem i s'eliminen per l'altre.

3. **Cua de prioritat**:
   - Els elements s'ordenen segons el seu valor de prioritat.

4. **Pila**:
   - Estructura LIFO (Last In First Out), on els elements s'afegeixen i s'eliminen pel mateix extrem.

---

## Complexitat temporal i espacial

- La **complexitat temporal** mesura el temps d'execució d'un algorisme en funció de la mida de les dades d'entrada.
- La **complexitat espacial** mesura l'espai en memòria que necessita un algorisme.

---

## Exemples de notació asimptòtica

- **O(1)**: Constant. Accés a un element d'un vector.
- **O(log n)**: Logarítmica. Cerca binària.
- **O(n)**: Lineal. Recorregut d'un vector.
- **O(n log n)**: Quasi-lineal. Algorisme de mergesort.
- **O(n^2)**: Polinòmica. Recorregut d'una matriu.
