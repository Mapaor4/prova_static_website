# Prova de web estàtica
Aquesta és la prova d'intentar crear una web estàtica a partir de continguts exportats de Notion (ja sigui amb HTML o Markdown, el que funcioni millor).
## Link web publicada
[Clicar aquí per anar a la web](https://mapaor4.github.io/prova_static_website/nav.html)
## Proves
Estil en general funciona prou bé, els links funcionen també. Veure [Funció gamma](https://mapaor4.github.io/prova_static_website/funcio_gamma.html).
Nota 1: El custom vídeo (i imagino que amb les imatges passarà el mateix) s'ha de modificar l'html per tal de incloure'l
Nota 2: La separació entre els toggle headings 1 és massa petita, s'hauria de modificar.
**Objectiu a la vista**: 
- *Aconseguir distingir fàcilment quina part és CSS i quina és HTML.*
- *Fer un estil CSS genèric per tots els fitxers (tipografia disseny etc).*
- *Aconseguir simplificar la part de Katex de manera que no calgui estar a cada fitxer HTML sinó en un genèric javascript*
- *Mirar si un cop conegut el CSS, al importar des de Markdown es pot simplificar i aconseguir que quedi el mateix look*
- *Markdown és per visualitzar des de Github o des de Jupyter o des de [MkDocs](https://www.mkdocs.org/user-guide/deploying-your-docs/). No sembla que es puguin posar toggle headings i no sé perquè moltes expressions matemàtiques no semblen renderitzar (malgrat moltes altres sí). Tot i així em sona que sí haurien de ser possibles els toggles normals, i ja miraré si es pot posar embeds, que no fa pinta. De moment pinta que lo xulo és HTML i Markdown ignorar-lo*
Al final l'ideal seria: Una persona random fa una pàgina en Notion, li dona a exportar HTML i l'afageix a un repositori de Github. Automàticament aquesta queda amb un bon disseny i linkada a les altres.
Nota xula: de veritat que estic flipant que funcioni tot tan bé i sigui tan fàcil.
## Procés que hauria d'anar fent
1. Posar un fitxer html senzill
2. Publicar-ho a lo github pages
3. Provar-ho després amb un fitxer markdown
4. Mirar-se lo de Jekyll i diguéssim el tipus de CSS que fa que el fitxer markdown es vegi estèticament xulo
5. Mirar-se com fer la web navegable (menú superior o similar) i no simplement pàgines solitàries independents
6. Provar si a part del text i els headings, les imatges queden ben incrustades, o com s'han de gestionar aquestes
7. Provar d'afegir-hi Katex (tal com als fitxers de admonitions, amb un script senzill) i mirar com queden els blocs de equacions i sobretot (el que em preocupa més) aviam com queden les inline equations.

