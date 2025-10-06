<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>RP-Gesetzbuch — In-Character</title>
  <style>
    /* Schwarz-Weiß, modernes, klares Layout */
    :root{
      --bg:#ffffff;
      --paper:#f7f7f7;
      --text:#0b0b0b;
      --muted:#6b6b6b;
      --accent:#000000;
      --border:#e6e6e6;
      --max-width:1100px;
    }
    html,body{
      height:100%;
      margin:0;
      font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background:linear-gradient(180deg,var(--bg),var(--paper));
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
    }

    .container{
      max-width:var(--max-width);
      margin:36px auto;
      padding:28px;
      background:#ffffff;
      border:1px solid var(--border);
      box-shadow:0 8px 30px rgba(0,0,0,0.04);
    }

    header{
      display:flex;
      align-items:baseline;
      justify-content:space-between;
      gap:18px;
      margin-bottom:20px;
    }
    header h1{
      font-size:22px;
      margin:0;
      letter-spacing:0.2px;
    }
    header p{
      margin:0;
      color:var(--muted);
      font-size:13px;
    }

    nav.toc{
      margin:18px 0 24px 0;
      padding:12px;
      background:transparent;
      border-left:3px solid var(--accent);
    }
    nav.toc ul{
      margin:0;
      padding:0 0 0 14px;
    }
    nav.toc li{
      list-style:none;
      font-size:14px;
      margin:6px 0;
      color:var(--muted);
    }
    nav.toc a{
      text-decoration:none;
      color:var(--text);
    }

    section{
      margin-bottom:22px;
    }
    h2{
      font-size:16px;
      margin:12px 0 10px 0;
      border-bottom:1px dashed var(--border);
      padding-bottom:8px;
    }
    .para{
      margin:8px 0 12px 0;
      white-space:pre-wrap;
      font-size:14px;
    }
    .para .sig{
      color:var(--muted);
      font-size:13px;
    }

    /* Tabelle für Delikte */
    table.offenses{
      width:100%;
      border-collapse:collapse;
      margin-top:10px;
      font-size:14px;
    }
    table.offenses thead th{
      text-align:left;
      padding:10px 12px;
      border-bottom:2px solid var(--border);
      background:transparent;
      font-weight:600;
      color:var(--text);
    }
    table.offenses tbody td{
      padding:10px 12px;
      border-bottom:1px solid var(--border);
      vertical-align:top;
    }
    table.offenses tbody tr:last-child td{ border-bottom:0; }

    .tag{
      display:inline-block;
      padding:6px 8px;
      font-size:12px;
      border:1px solid var(--border);
      background:#fff;
      color:var(--muted);
      border-radius:6px;
    }

    footer{
      margin-top:24px;
      font-size:13px;
      color:var(--muted);
      border-top:1px dashed var(--border);
      padding-top:12px;
      display:flex;
      justify-content:space-between;
      gap:12px;
    }

    /* Responsive */
    @media (max-width:800px){
      .container{ padding:18px; margin:18px; }
      header{ flex-direction:column; align-items:flex-start; gap:6px; }
      table.offenses thead{ display:none; }
      table.offenses tbody td{ display:block; padding:10px 0; }
      table.offenses tbody td::before{ content:attr(data-label); font-weight:600; display:block; margin-bottom:6px; color:var(--muted); }
    }
  </style>
</head>
<body>
  <div class="container" role="main">
    <header>
      <div>
        <h1>RP-Gesetzbuch (In-Character)</h1>
        <p>Rechtsgrundlagen, Straftatbestände, Haftzeiten und Bußgelder — realistisch für RP-Server. Beträge in Euro (€).</p>
      </div>
      <div class="meta">
        <p class="tag">Max. Haftzeit: 180 Minuten (Terroranschlag)</p>
        <p class="tag" style="margin-left:8px">Max. Bußgeld: 50.000 €</p>
      </div>
    </header>

    <nav class="toc" aria-label="Inhaltsverzeichnis">
      <strong>Inhaltsverzeichnis</strong>
      <ul>
        <li><a href="#allgemeines">§1–§3 Allgemeines & Bürgerrechte</a></li>
        <li><a href="#strafrecht">§4–§9 Strafrecht</a></li>
        <li><a href="#verkehr">§10–§14 Verkehrsrecht</a></li>
        <li><a href="#waffen">§15–§17 Waffen & Drogen</a></li>
        <li><a href="#staatsgefahr">§18–§19 Staatsgefährdung</a></li>
        <li><a href="#gericht">§20–§22 Gericht & Strafen</a></li>
        <li><a href="#uebersicht">Übersicht: Sanktionen & Bußgelder (Tabelle)</a></li>
      </ul>
    </nav>

    <section id="allgemeines">
      <h2>Abschnitt I — Allgemeines Staatsrecht</h2>

      <div class="para">
        §1 Staatsordnung
        (1) Der Staat dient dem Schutz der Bürger, der Aufrechterhaltung der öffentlichen Ordnung und dem Gemeinwohl.
        (2) Staatsgewalt wird entlang der Gewaltenteilung (Exekutive, Legislative, Judikative) ausgeübt.
      </div>

      <div class="para">
        §2 Bürgerrechte
        (1) Jeder Bürger hat das Recht auf Leben, Freiheit und körperliche Unversehrtheit.
        (2) Gleichheit vor dem Gesetz ist gewährleistet.
        (3) Meinungsäußerungen sind zulässig, solange sie nicht gegen strafrechtliche Tatbestände verstoßen.
      </div>

      <div class="para">
        §3 Öffentliche Ordnung
        (1) Verhalten in der Öffentlichkeit muss die Sicherheit und das Wohl anderer beachten.
        (2) Waffen, gefährliche Gegenstände oder das Führen solcher ohne Berechtigung sind untersagt.
      </div>
    </section>

    <section id="strafrecht">
      <h2>Abschnitt II — Strafrecht</h2>

      <div class="para">
        §4 Körperverletzung
        (1) Vorsätzliche Körperverletzung zieht eine Freiheitsentziehung oder Geldstrafe nach sich.
        (2) Normales Strafmaß: 10–60 Minuten Haft oder 500–6.000 € Geldstrafe, abhängig von Schwere und Wiederholung.
        (3) Schwere Fälle (Waffe, dauerhafte Schäden): 60–120 Minuten Haft oder 5.000–20.000 €.
      </div>

      <div class="para">
        §5 Mord und Totschlag
        (1) Tötungsdelikte sind die schwersten Straftaten. Mord (vorsätzlich + geplant) zieht hohe Höchststrafen nach sich.
        (2) Maß: 120–180 Minuten Haft bei besonders schweren Taten; Bußgelder sind symbolisch und geringer relevant.
      </div>

      <div class="para">
        §6 Diebstahl und Raub
        (1) Diebstahl: 5–40 Minuten Haft oder 250–4.000 €.
        (2) Raub (mit Gewalt oder Drohung): 30–120 Minuten Haft oder 2.000–15.000 €.
        (3) Schwerer Raub (Waffen, schwerer Schaden): 90–150 Minuten Haft, bis 30.000 €.
      </div>

      <div class="para">
        §7 Betrug
        (1) Täuschung zur Vermögensverschaffung: 20–100 Minuten Haft oder 1.000–25.000 €, abhängig vom Schaden.
      </div>

      <div class="para">
        §8 Sachbeschädigung
        (1) Zerstörung/Schädigung fremden Eigentums: 10–80 Minuten Haft oder 500–10.000 €, je nach Schadenshöhe.
      </div>

      <div class="para">
        §9 Amtsanmaßung und Korruption
        (1) Amtsanmaßung: 30–120 Minuten Haft und bis zu 10.000 € Bußgeld.
        (2) Korruption: Bestechung von Amtsträgern und Bestechlichkeit: 60–150 Minuten Haft und bis zu 50.000 €.
      </div>
    </section>

    <section id="verkehr">
      <h2>Abschnitt III — Verkehrsrecht</h2>

      <div class="para">
        §10 Allgemeine Vorschriften
        (1) Fahrerlaubnis ist erforderlich; Rücksichtnahme und Verkehrssicherheit sind Pflicht.
        (2) Alkohol-/Drogenfahrt: 30–120 Minuten Haft, Bußgeld 1.000–10.000 €.
      </div>

      <div class="para">
        §11 Geschwindigkeitsüberschreitungen
        (1) Innerorts übliche Grenze: 50 km/h (RP-Standard). Überschreitungen ziehen Bußgelder und ggf. Haft nach sich.
        (2) Maß: leichte Übertretung 0–20 km/h: Verwarnung oder bis 300 €; grobe Übertretung: 30–90 Minuten Haft und bis 5.000 €.
      </div>

      <div class="para">
        §12 Unfallflucht
        (1) Fahrerflucht: 60–150 Minuten Haft und 2.000–25.000 € Bußgeld; Fahrzeugbeschlagnahme möglich.
      </div>

      <div class="para">
        §13 Illegale Rennen
        (1) Teilnahme an Straßenrennen: 40–120 Minuten Haft, Fahrzeugbeschlagnahme und 2.000–20.000 €.
      </div>
    </section>

    <section id="waffen">
      <h2>Abschnitt IV — Waffen- und Drogenrecht</h2>

      <div class="para">
        §14 Waffenbesitz
        (1) Besitz/Führen ohne Lizenz: 60–150 Minuten Haft, 2.000–25.000 €.
        (2) Illegale Schusswaffen: harte Maßnahmen, 120–180 Minuten Haft und bis zu 50.000 €.
      </div>

      <div class="para">
        §15 Drogenbesitz und Handel
        (1) Besitz kleiner Mengen (Eigengebrauch): 10–40 Minuten Haft oder 250–2.000 €.
        (2) Handel/Herstellung/Großmengen: 90–180 Minuten Haft und 5.000–50.000 €.
      </div>
    </section>

    <section id="staatsgefahr">
      <h2>Abschnitt V — Staatsgefährdung</h2>

      <div class="para">
        §16 Widerstand gegen Staatsgewalt
        (1) Gewalt oder Drohung gegenüber Beamten: 60–150 Minuten Haft und 2.000–25.000 €.
      </div>

      <div class="para">
        §17 Terroristische Handlungen
        (1) Planung, Unterstützung oder Ausführung von Anschlägen: Höchstmaß der Sanktionen.
        (2) Maß: 120–180 Minuten Haft; Bußgeld bis 50.000 €. Zusätzlich stehen besondere Maßnahmen der Staatsorgane zur Verfügung.
      </div>

      <div class="para">
        §18 Staatsverrat
        (1) Verrat von relevanten Staatsgeheimnissen oder aktive Zusammenarbeit mit Feinden: 150–180 Minuten Haft; Bußgelder bis 50.000 €.
      </div>
    </section>

    <section id="gericht">
      <h2>Abschnitt VI — Gericht und Strafen</h2>

      <div class="para">
        §19 Zuständigkeit
        (1) Gerichte entscheiden nach vorgelegten Beweisen; Polizei ermittelt und bringt Verdächtige vor Gericht.
        (2) Bei leichten Vergehen kann die Polizei Bußgelder oder Verwarnungen aussprechen.
      </div>

      <div class="para">
        §20 Strafmaße und Kombinationen
        (1) Strafen können kombiniert werden: Haftzeit plus Geldstrafe.
        (2) Wiederholungstäter erhalten erhöhte Strafmaße (multiplikatorisch).
      </div>

      <div class="para">
        §21 Rehabilitation
        (1) Nach Verbüßung oder Zahlung der Strafmaßnahmen gelten Betroffene wieder als rechtskonform.
        (2) Gerichtliche Tilgung oder Entschuldigungen sind möglich, sofern Reue und Wiedergutmachung erfolgen.
      </div>
    </section>

    <section id="uebersicht">
      <h2>Übersicht: Sanktionen & Bußgelder</h2>
      <p class="para">Die folgende Tabelle gibt eine schnelle Übersicht gängiger Delikte mit empfohlenen Mindest- und Höchststrafen. Alle Beträge in Euro (€), Haftzeiten in Minuten.</p>

      <table class="offenses" aria-describedby="uebersicht">
        <thead>
          <tr>
            <th>Delikt</th>
            <th>Haftzeit (min)</th>
            <th>Bußgeld (€)</th>
            <th>Bemerkung</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td data-label="Delikt">Körperverletzung (leicht)</td>
            <td data-label="Haftzeit">10 – 60</td>
            <td data-label="Bußgeld">500 – 6.000</td>
            <td data-label="Bemerkung">Abhängig von Verletzungsgrad</td>
          </tr>
          <tr>
            <td data-label="Delikt">Körperverletzung (schwer)</td>
            <td data-label="Haftzeit">60 – 120</td>
            <td data-label="Bußgeld">5.000 – 20.000</td>
            <td data-label="Bemerkung">Waffe, bleibende Schäden</td>
          </tr>
          <tr>
            <td data-label="Delikt">Diebstahl</td>
            <td data-label="Haftzeit">5 – 40</td>
            <td data-label="Bußgeld">250 – 4.000</td>
            <td data-label="Bemerkung">Wertabhängig</td>
          </tr>
          <tr>
            <td data-label="Delikt">Raub</td>
            <td data-label="Haftzeit">30 – 120</td>
            <td data-label="Bußgeld">2.000 – 15.000</td>
            <td data-label="Bemerkung">Gewalt oder Drohung</td>
          </tr>
          <tr>
            <td data-label="Delikt">Betrug</td>
            <td data-label="Haftzeit">20 – 100</td>
            <td data-label="Bußgeld">1.000 – 25.000</td>
            <td data-label="Bemerkung">Schadenrelevant</td>
          </tr>
          <tr>
            <td data-label="Delikt">Sachbeschädigung</td>
            <td data-label="Haftzeit">10 – 80</td>
            <td data-label="Bußgeld">500 – 10.000</td>
            <td data-label="Bemerkung">Inkl. staatl. Eigentum</td>
          </tr>
          <tr>
            <td data-label="Delikt">Waffenbesitz illegal</td>
            <td data-label="Haftzeit">60 – 150</td>
            <td data-label="Bußgeld">2.000 – 25.000</td>
            <td data-label="Bemerkung">Illegale Schusswaffen härter</td>
          </tr>
          <tr>
            <td data-label="Delikt">Drogenhandel (Groß)</td>
            <td data-label="Haftzeit">90 – 180</td>
            <td data-label="Bußgeld">5.000 – 50.000</td>
            <td data-label="Bemerkung">Handel/Herstellung</td>
          </tr>
          <tr>
            <td data-label="Delikt">Terroranschlag / schwere Staatsgefährdung</td>
            <td data-label="Haftzeit">120 – 180</td>
            <td data-label="Bußgeld">10.000 – 50.000</td>
            <td data-label="Bemerkung">Höchste Sanktionen</td>
          </tr>
          <tr>
            <td data-label="Delikt">Fahrerflucht</td>
            <td data-label="Haftzeit">60 – 150</td>
            <td data-label="Bußgeld">2.000 – 25.000</td>
            <td data-label="Bemerkung">Fahrzeugbeschlagnahme möglich</td>
          </tr>
          <tr>
            <td data-label="Delikt">Illegale Straßenrennen</td>
            <td data-label="Haftzeit">40 – 120</td>
            <td data-label="Bußgeld">2.000 – 20.000</td>
            <td data-label="Bemerkung">Gefahrenabwehr</td>
          </tr>
        </tbody>
      </table>
    </section>

    <footer>
      <div>Dieses Gesetzbuch ist IC (In-Character) konzipiert und dient als Referenz für RP-Akteure.</div>
      <div>Stand: automatisch generiert · Beträge in € · Max. Haft: 180 Minuten · Max. Bußgeld: 50.000 €</div>
    </footer>
  </div>
</body>
</html>
