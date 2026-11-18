# Mòdul Odoo: Cinema

Mòdul d'Odoo per gestionar un catàleg de pel·lícules, directors i actors. Correspon a la pràctica d'examen de maig de 2025 de l'assignatura de Sistemes de Gestió Empresarial (SGE) del CFGS de Desenvolupament d'Aplicacions Multiplataforma (Institut Milà i Fontanals, Igualada).

## Models

- **`cinema.person`**: persones del cinema (nom, cognoms, gènere, dates de naixement i defunció, nacionalitat). Es poden marcar com a director i/o actor. El nom complet es calcula automàticament.
- **`cinema.film`**: pel·lícules (títol traduïble, any, durada, sinopsi, pàgina web, pòster, director i actors). El tipus de pel·lícula es calcula a partir de la durada.
- **`res.country`** (ampliat): compta quants directors té cada país i els mostra a la fitxa del país.

## Regles de negoci

- La data de defunció no pot ser anterior a la de naixement.
- No poden existir dues persones amb el mateix nom, cognoms i data de naixement (índex únic).
- No es pot eliminar una persona vinculada a pel·lícules com a director o actor.

## Altres elements

- Vistes de llista, formulari i cerca, i menús propis.
- Informe PDF de pel·lícula (`report/cinema_film_report.xml`).
- Grups i permisos d'accés (`security/`).
- Dades de demostració (`demo/demo_data.xml`).

## Instal·lació

1. Copia la carpeta del mòdul al directori `addons` d'Odoo (o afegeix-ne la ruta a `addons_path`).
2. Reinicia el servidor i actualitza la llista d'aplicacions.
3. Instal·la l'aplicació **cinema_maig2025**. Depèn només del mòdul `base`.

## Autoria

Sara Prats Morales · Llicència LGPL-3
