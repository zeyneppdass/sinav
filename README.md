<html><head><meta charset="utf8"><meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Rehberlik Testi</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@500&amp;family=IBM+Plex+Sans:wght@400;500;600&amp;display=swap">
<style>
/* Layout: tek sütun test kâğıdı; sabit sayaç çubuğu, 50 soruluk gezgin, sonuçta konu bazlı tablo. Vurgu tek mavi; durum renkleri ayrı. */
:root {
  --bg: #F4F5F8;
  --surface: #FFFFFF;
  --fg: #17202C;
  --muted: #586374;
  --line: #D8DDE5;
  --accent: #2548C8;
  --accent-fg: #FFFFFF;
  --accent-soft: #E6ECFD;
  --good: #146C43;
  --good-bg: #E1F3E8;
  --bad: #AE2A21;
  --bad-bg: #FBE6E3;
  --warn: #8A5700;
  --warn-bg: #FFF1D6;
  --font-text: "IBM Plex Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  --font-mono: "IBM Plex Mono", ui-monospace, Menlo, Consolas, monospace;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #10151B; --surface: #181F28; --fg: #E7EBF1; --muted: #9AA5B5; --line: #2A3340;
    --accent: #8BA4FF; --accent-fg: #0A1030; --accent-soft: #212C4E;
    --good: #62CF95; --good-bg: #163322; --bad: #FF9087; --bad-bg: #3A1D1B; --warn: #F0BE63; --warn-bg: #3A2D10;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #10151B; --surface: #181F28; --fg: #E7EBF1; --muted: #9AA5B5; --line: #2A3340;
  --accent: #8BA4FF; --accent-fg: #0A1030; --accent-soft: #212C4E;
  --good: #62CF95; --good-bg: #163322; --bad: #FF9087; --bad-bg: #3A1D1B; --warn: #F0BE63; --warn-bg: #3A2D10;
  color-scheme: dark;
}
* { box-sizing: border-box; }
body {
  background: var(--bg); color: var(--fg);
  font-family: var(--font-text); font-size: 16px; line-height: 1.55;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  padding-block: 20px 56px;
}
body::before { content: ""; position: fixed; inset: 0 0 auto; height: env(safe-area-inset-top, 0px); z-index: 10; background: var(--surface); }
.wrap { max-width: 760px; margin: 0 auto; display: grid; gap: 16px; }
h1, h2, p { margin: 0; }
h1 { font-size: clamp(1.6rem, 4.5vw, 2.1rem); line-height: 1.2; font-weight: 600; text-wrap: balance; letter-spacing: -0.01em; }
h2 { font-size: 1.15rem; font-weight: 600; text-wrap: balance; }
.eyebrow { font-size: .75rem; letter-spacing: .08em; text-transform: uppercase; color: var(--muted); font-weight: 600; }
.mono { font-family: var(--font-mono); font-variant-numeric: tabular-nums; }
button { font: inherit; cursor: pointer; }
:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }

.sheet { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 24px; display: grid; gap: 18px; min-width: 0; }
.meta { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: var(--line); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; }
.meta div { background: var(--surface); padding: 10px 14px; display: grid; gap: 2px; }
.meta b { font-size: 1.15rem; font-weight: 600; }
.meta span { font-size: .75rem; color: var(--muted); letter-spacing: .04em; text-transform: uppercase; }
.table-scroll { overflow-x: auto; }
table { border-collapse: collapse; width: 100%; font-size: .95rem; }
th, td { text-align: left; padding: 8px 10px; border-bottom: 1px solid var(--line); }
th { font-size: .75rem; letter-spacing: .06em; text-transform: uppercase; color: var(--muted); font-weight: 600; }
td.num, th.num { text-align: right; font-variant-numeric: tabular-nums; white-space: nowrap; }
.field { display: grid; gap: 6px; }
.field label { font-size: .85rem; font-weight: 500; color: var(--muted); }
input[type=text] { font: inherit; color: var(--fg); background: var(--bg); border: 1px solid var(--line); border-radius: 8px; padding: 10px 12px; width: 100%; }
.btn { background: var(--accent); color: var(--accent-fg); border: 1px solid var(--accent); border-radius: 8px; padding: 10px 18px; font-weight: 600; }
.btn.ghost { background: transparent; color: var(--fg); border-color: var(--line); }
.btn:hover { filter: brightness(1.06); }
.rules { color: var(--muted); font-size: .92rem; padding-left: 1.1em; margin: 0; display: grid; gap: 4px; }

.bar { position: sticky; top: env(safe-area-inset-top, 0px); z-index: 5; background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 10px 14px; display: flex; flex-wrap: wrap; align-items: center; gap: 10px 16px; }
.timer { font-family: var(--font-mono); font-size: 1.3rem; font-weight: 500; font-variant-numeric: tabular-nums; }
.timer.low { color: var(--bad); }
.prog { flex: 1 1 140px; display: grid; gap: 4px; min-width: 0; }
.prog small { color: var(--muted); font-size: .8rem; }
.track { height: 6px; background: var(--line); border-radius: 3px; overflow: hidden; }
.track i { display: block; height: 100%; width: 0; background: var(--accent); transition: width .2s; }
.navgrid { display: flex; flex-wrap: wrap; gap: 6px; }
.navgrid button { width: 38px; height: 34px; border: 1px solid var(--line); background: var(--surface); color: var(--fg); border-radius: 6px; font-family: var(--font-mono); font-size: .85rem; }
.navgrid button.done { background: var(--accent-soft); border-color: var(--accent); color: var(--accent); }

.q { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 18px 20px; display: grid; gap: 14px; scroll-margin-top: 110px; min-width: 0; }
.qhead { display: grid; grid-template-columns: auto 1fr; gap: 12px; align-items: start; }
.qn { font-family: var(--font-mono); font-size: .95rem; background: var(--accent-soft); color: var(--accent); border-radius: 6px; min-width: 34px; text-align: center; padding: 2px 8px; }
.qt { overflow-wrap: anywhere; }
.opts { display: grid; gap: 8px; }
.opt { display: grid; grid-template-columns: auto auto 1fr; gap: 10px; align-items: start; border: 1px solid var(--line); border-radius: 8px; padding: 10px 12px; cursor: pointer; min-width: 0; }
.opt input { accent-color: var(--accent); margin-top: 4px; }
.opt .ol { font-family: var(--font-mono); color: var(--muted); }
.opt.sel { background: var(--accent-soft); border-color: var(--accent); }
.opt span:last-child { overflow-wrap: anywhere; }
.endrow { display: flex; flex-wrap: wrap; gap: 12px; align-items: center; justify-content: space-between; }
.exp { color: var(--muted); font-size: .92rem; }

#confirm { position: fixed; left: 0; right: 0; bottom: 0; z-index: 20; background: var(--surface); border-top: 1px solid var(--line); padding: 14px max(16px, env(safe-area-inset-left, 0px)) calc(14px + env(safe-area-inset-bottom, 0px)); }
#confirm > div { max-width: 760px; margin: 0 auto; display: flex; flex-wrap: wrap; gap: 12px; align-items: center; justify-content: space-between; }
#confirm p { flex: 1 1 260px; }
#confirm .acts { display: flex; gap: 8px; }

.total { display: flex; flex-wrap: wrap; align-items: baseline; gap: 6px 14px; }
.total .big { font-family: var(--font-mono); font-size: clamp(2.6rem, 9vw, 3.6rem); font-weight: 500; line-height: 1; font-variant-numeric: tabular-nums; }
.total span { color: var(--muted); }
.counts { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: var(--line); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; }
.counts div { background: var(--surface); padding: 10px 14px; display: grid; gap: 2px; }
.counts b { font-family: var(--font-mono); font-size: 1.3rem; font-weight: 500; }
.counts span { font-size: .75rem; color: var(--muted); letter-spacing: .04em; text-transform: uppercase; }
.counts .g b { color: var(--good); } .counts .r b { color: var(--bad); } .counts .y b { color: var(--warn); }
.minibar { height: 8px; min-width: 90px; background: var(--line); border-radius: 4px; overflow: hidden; }
.minibar i { display: block; height: 100%; background: var(--accent); }
.filters { display: flex; flex-wrap: wrap; gap: 8px; }
.filters button { background: var(--surface); color: var(--fg); border: 1px solid var(--line); border-radius: 99px; padding: 6px 14px; font-size: .9rem; }
.filters button[aria-pressed="true"] { background: var(--accent-soft); color: var(--accent); border-color: var(--accent); font-weight: 600; }
.rv { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 18px 20px; display: grid; gap: 12px; min-width: 0; }
.rvhead { display: grid; grid-template-columns: auto 1fr auto; gap: 12px; align-items: start; }
.pill { font-size: .78rem; font-weight: 600; padding: 2px 10px; border-radius: 99px; white-space: nowrap; align-self: start; }
.pill.ok { background: var(--good-bg); color: var(--good); }
.pill.no { background: var(--bad-bg); color: var(--bad); }
.pill.blank { background: var(--warn-bg); color: var(--warn); }
.ropts { list-style: none; margin: 0; padding: 0; display: grid; gap: 6px; }
.ropts li { border: 1px solid var(--line); border-radius: 8px; padding: 8px 12px; display: flex; flex-wrap: wrap; gap: 4px 10px; justify-content: space-between; }
.ropts li.ok { background: var(--good-bg); border-color: var(--good); }
.ropts li.no { background: var(--bad-bg); border-color: var(--bad); }
.ropts .tag { font-size: .78rem; font-weight: 600; }
.topic { font-size: .75rem; letter-spacing: .06em; text-transform: uppercase; color: var(--muted); font-weight: 600; }
.empty { color: var(--muted); padding: 12px 0; }

@media (max-width: 520px) {
  .meta { grid-template-columns: 1fr; }
  .sheet, .q, .rv { padding: 16px; }
}
@media (prefers-reduced-motion: reduce) { .track i { transition: none; } }
</style>

<main class="wrap">
  <section id="intro" class="sheet" aria-labelledby="introTitle">
    <div>
      <p class="eyebrow">Test sınavı</p>
      <h1 id="introTitle">Rehberlik ve Psikolojik Danışma</h1>
    </div>
    <div class="meta">
      <div><b>75 dk</b><span>Süre</span></div>
      <div><b>50 soru</b><span>Beş seçenekli</span></div>
      <div><b>100</b><span>Toplam puan</span></div>
    </div>
    <div class="table-scroll">
      <table>
        <thead><tr><th>Konu</th><th class="num">Soru</th></tr></thead>
        <tbody>
          <tr><td>Rehberliğin tanımı, amacı ve ilkeleri</td><td class="num">11</td></tr>
          <tr><td>Rehberlik modelleri ve eğitim anlayışları</td><td class="num">10</td></tr>
          <tr><td>Kapsamlı PDR programı</td><td class="num">9</td></tr>
          <tr><td>Rehberlik türleri</td><td class="num">10</td></tr>
          <tr><td>Eğitsel rehberlik ve sınav kaygısı</td><td class="num">4</td></tr>
          <tr><td>Rehberlik hizmetleri (ÖKH)</td><td class="num">6</td></tr>
        </tbody>
      </table>
    </div>
    <ul class="rules">
      <li>Her soru 2 puandır; yanlış cevap doğruyu götürmez.</li>
      <li>Seçenekler her denemede farklı sırayla gelir.</li>
      <li>Süre dolunca test kendiliğinden biter. Sonuçta konu bazlı başarını ve her sorunun açıklamasını görürsün.</li>
    </ul>
    <div class="field">
      <label for="studentName">Ad Soyad (isteğe bağlı)</label>
      <input type="text" id="studentName" autocomplete="off">
    </div>
    <div><button class="btn" id="startBtn" type="button">Testi başlat</button></div>
  </section>

  <section id="exam" hidden="">
    <div class="wrap">
      <div class="bar" role="group" aria-label="Test durumu">
        <div class="timer" id="timer" role="timer" aria-live="off">75:00</div>
        <div class="prog">
          <small id="progText">0 / 50 cevaplandı</small>
          <div class="track"><i id="progBar"></i></div>
        </div>
        <button class="btn ghost" id="finishTop" type="button">Bitir</button>
      </div>
      <nav class="navgrid" id="navgrid" aria-label="Soru gezgini"></nav>
      <div id="questions" class="wrap"></div>
      <div class="endrow">
        <p class="exp" id="leftText"></p>
        <button class="btn" id="finishBottom" type="button">Testi bitir</button>
      </div>
    </div>
  </section>

  <section id="result" hidden=""></section>
</main>

<div id="confirm" hidden="">
  <div>
    <p id="confirmText"></p>
    <div class="acts">
      <button class="btn ghost" id="confirmNo" type="button">Teste dön</button>
      <button class="btn" id="confirmYes" type="button">Evet, bitir</button>
    </div>
  </div>
</div>

<script>
(function () {
  var DURATION = 75 * 60 * 1000;
  var PTS = 2;
  var TOPICS = ['Tanım, amaç ve ilkeler', 'Modeller ve eğitim anlayışları', 'Kapsamlı PDR programı', 'Rehberlik türleri', 'Eğitsel rehberlik ve sınav kaygısı', 'Rehberlik hizmetleri (ÖKH)'];

  /* [konu, soru, doğru şık, yanlış 1-4, açıklama] — şıklar her denemede karıştırılır */
  var RAW = [
    [0,"Rehberliğin nihai (sonal) amacı aşağıdakilerden hangisidir?","Bireyin kendini gerçekleştirmesine yardımcı olmak","Bireyi disipline etmek","Bireyin sorunlarını onun adına çözmek","Yalnızca akademik başarıyı artırmak","Bireyi bir mesleğe yerleştirmek","Rehberliğin nihai amacı, bireyin kendinde var olan gizli potansiyeli açığa çıkararak kendini gerçekleştirmesine yardım etmektir. Bu amaca ulaşmak için önce alt amaçlar gerçekleştirilir."],
    [0,"“Kendini gerçekleştirme” kavramının karşılığı olarak slaytlarda verilen terim hangisidir?","Tam işlerlik","Tam bağımsızlık","Tam uyum","Tam başarı","Tam denetim","Kendini gerçekleştirme, bireyin her yönüyle kapasitesini sonuna dek geliştirebilmesi anlamında “tam işlerlik” olarak ifade edilir ve yaşam boyu sürer."],
    [0,"Rehberlik hizmetlerinin birinci (birincil) işlevi aşağıdakilerden hangisidir?","Bireyin kendini tanımasını sağlamak","Bireye öğüt ve nasihat vermek","Bireyin sorunlarını hemen çözmek","Bireyi kontrol altında tutmak","Bireyin yerine karar vermek","İlk işlev, bireyin kendini tanıması, anlaması ve kabul etmesine yardım etmektir; bu, bireyi tanıma çalışmalarıyla sağlanır."],
    [0,"Rehberliğin üçüncü işlevi aşağıdakilerden hangisidir?","Bireyin potansiyellerini uygun çevre koşullarında kullanmasına yardım etmek","Bireyin kendini tanımasına yardım etmek","Bireyin çevresindeki imkânları fark etmesine yardım etmek","Bireyi disipline etmek","Bireyin sorunlarını onun adına çözmek","Üçüncü işlev, birinci (kendini tanıma) ve ikinci (çevredeki imkânları fark etme) işlevi uzlaştırarak potansiyelin uygun çevre koşullarında kullanılmasına yardım etmektir."],
    [0,"Aşağıdakilerden hangisi gizlilik ilkesinin istisnası sayılır?","Danışanın hayatını tehlikeye sokan bir durumun (intihar, istismar gibi) ortaya çıkması","Öğrencinin ders notlarının düşük olması","Velinin öğrenci hakkında bilgi istemesi","Öğretmenin öğrenciyi merak etmesi","Öğrencinin meslek tercihinin açıklanması","Hayati tehlike varsa danışanın izni alınmadan, ama danışan önceden haberdar edilerek gerekli kişilere bilgi verilir."],
    [0,"Rehberlik hizmetlerinde “gönüllülük” ilkesi ile aşağıdakilerden hangisi ifade edilir?","Öğrenci yararlanmaya teşvik edilir ancak zorlanamaz","Öğrenci gerekirse zorla danışmaya gönderilir","Öğrencinin yararlanması için baskı yapılabilir","Hizmet yalnızca yöneticinin isteğiyle verilir","Hizmeti almayan öğrenciye ceza verilir","Hizmetler sunulur, öğrenci yararlanmaya teşvik edilir; ancak zorlanamaz, zorla danışmaya gönderilemez ve seçim yapması için baskılanamaz."],
    [0,"Aşağıdakilerden hangisi rehberlik ve psikolojik danışma için doğru DEĞİLDİR?","Tüm problemleri hemen çözebilecek sihirli bir güce sahiptir","Bireyi yargılamaz ve ceza vermez","Bireye yol değil, yollar gösterir","Son karar bireye aittir","Gönüllülüğe dayalı bir hizmettir","Rehberlik ve psikolojik danışma tüm problemleri hemen çözebilecek sihirli bir güce sahip değildir."],
    [0,"Rehberliğin bireyi disipline etme (kontrol) görevi olmadığı belirtilir. Çağdaş eğitimde temel olan aşağıdakilerden hangisidir?","İç disiplin ya da içten denetim","Dıştan sıkı denetim","Ödül-ceza sistemi","Okul kurallarının baskıyla uygulanması","Öğretmenin tek yönlü otoritesi","Çağdaş eğitimde temel olan iç disiplin ya da içten denetimdir."],
    [0,"Slaytlardaki Maslow ihtiyaçlar hiyerarşisinde üst düzey/gelişimsel ihtiyaçlar hangi hizmetlerle ilişkilendirilmiştir?","PDR hizmetleri","Sağlık hizmetleri","Sosyal yardım hizmetleri","Özel eğitim hizmetleri","Sosyal-kültürel hizmetler","Slaytta üst düzey/gelişimsel ihtiyaçlar PDR hizmetleriyle, alt düzey/temel ihtiyaçlar ise rehberlikle ilişkilendirilmiştir."],
    [0,"Aşağıdakilerden hangisi kendini gerçekleştiren bireyin özelliklerinden biri DEĞİLDİR?","Toplumsal kalıplara tamamen uyum gösterir","Kendini gerçekçi şekilde tanır","Yaratıcıdır veya üreticidir","Özerktir, çevresinden bağımsızdır","Düşmanca olmayan bir mizah anlayışına sahiptir","Kendini gerçekleştiren bireyler insanlarla birlikte olmaktan hoşlanır, fakat toplumsal kalıplara karşı çıkabilir ve kültürün etkisine direnebilir."],
    [0,"Rehberlik hizmetlerinin yürütülmesiyle ilgili aşağıdakilerden hangisi doğrudur?","Psikolojik danışman, öğretmen, yönetici, veli ve çevrenin işbirliğini gerektiren bir ekip çalışmasıdır","Yalnızca psikolojik danışman tarafından verilir","Yalnızca sınıf öğretmeni tarafından verilir","Yalnızca okul yöneticisinin sorumluluğundadır","Ekip çalışması gerektirmez","Rehberlik bir takım çalışmasıdır; rehberlik uzmanı, öğretmenler, veli, yöneticiler ve çevrenin işbirliği gerekir. Hizmeti herkes veremez ve sadece psikolojik danışman da vermez."],

    [1,"Frank Parsons'ın 1908'de başlattığı rehberlik çalışmasının amacı aşağıdakilerden hangisidir?","Endüstri bölgelerinde iş arayan vasıfsız göçmenlerin uygun bir işe yerleşmesine yardımcı olmak","Okullarda grup rehberliği saatleri koymak","Öğrencilerin sınav kaygısını azaltmak","Psikolojik testlerle tedavi uygulamak","Öğrencilere disiplin kazandırmak","Parsons, kısa bir eğitim programından geçtikten sonra vasıfsız göçmenlerin uygun işe yerleşmesine yardım etti; ilk rehberlik çalışması mesleki rehberliktir."],
    [1,"Parsons modelinin uyguladığı üç basamak hangi seçenekte doğru verilmiştir?","Bireyi tanıma – meslekleri tanıma – eşleştirme","Bireyi tanıma – tedavi – izleme","Oryantasyon – yöneltme – sevk","Test uygulama – karar verme – izleme","Bilgi verme – grup rehberliği – psikolojik danışma","Parsons modeli: bireyi inceleyerek tanıma, mesleklerin gerektirdiği niteliklerin incelenmesi (meslek analizi) ve birey özellikleri ile meslekler arasında eşleştirme."],
    [1,"“Eğitim ve rehberlik amaç, yöntem ve sonuçları bakımından aynıdır” görüşü hangi modele aittir?","Eğitimle kaynaştırılmış model (Brewer)","Klinik model (Williamson)","Parsons modeli","Karar vermeye yardım süreci modeli","Gelişimsel model","Brewer'a göre eğitim ve rehberlik özdeştir. Bu model sonucunda okul programlarında grup rehberliği için saatler ayrılmaya başlanmıştır."],
    [1,"Aşağıdakilerden hangisi klinik (özellik-faktör) modelin özelliğidir?","Sorunun nedenini ortaya çıkarmak çözümde en önemli aşamadır; ölçme araçları sıklıkla kullanılır","Rehberlik yalnızca meslek seçiminden ibarettir","Gelişim görevleri temel alınır","Okullarda grup rehberliği saatleri bu modelle başlamıştır","Rehberlik, bireyin karar verme sürecine yardımdır","Williamson'un klinik modeli, bireysel farklılıkları dikkate alır ve sorunun nedenini test, gözlem gibi ölçme araçlarıyla ortaya çıkarmaya ağırlık verir."],
    [1,"Rehberliği “bireyin karar verme sürecine yardım” olarak tanımlayan model temsilcileri aşağıdakilerden hangisidir?","Katz, Tiedeman, Jones, Tyler","Maslow, Rogers, Mathewson, Havighurst","Frank Parsons","Brewer","Williamson","Karar vermeye yardım süreci modelinin başlıca temsilcileri Katz, Tiedeman, Jones ve Tyler'dır."],
    [1,"Gelişimsel rehberlik anlayışı hangi dönemde ve neye tepki olarak ortaya çıkmıştır?","1960'larda, rehberliğin sorun çözmeye indirgenmesine tepki olarak","1908'de, mesleki rehberliğe tepki olarak","1930'larda, testlerin yaygınlaşmasına tepki olarak","1980'lerde, grup rehberliğine tepki olarak","2006'da, kapsamlı PDR programına tepki olarak","Gelişimsel rehberlik, rehberliğin akademik başarıyı artırma, program ve meslek seçimi gibi sorunlarla sınırlandırılmasına ve düzeltici yardımlara ağırlık verilmesine tepki olarak 1960'lı yıllarda ortaya çıkmıştır."],
    [1,"Günümüzde geçerli olan ve kullanılan, çağdaş eğitimin rehberlik modeli hangisidir?","Gelişimsel rehberlik","Parsons modeli","Klinik model","Eğitimle kaynaştırılmış model","Karar vermeye yardım süreci modeli","Gelişimsel rehberlik çağdaş eğitimin rehberlik modelidir; kapsamlı PDR programları bu yaklaşımın uygulama boyutudur."],
    [1,"“Gelişim süreklidir.” ilkesinden hareketle gelişimsel rehberlikte aşağıdakilerden hangisi savunulur?","Rehberlik hizmetleri kesintisiz yapılmalıdır","Rehberlik yalnızca kriz anlarında yapılmalıdır","Rehberlik yalnızca ortaöğretimde yapılmalıdır","Rehberlik yalnızca sorunlu öğrencilere yapılmalıdır","Rehberlik yalnızca sınav dönemlerinde yapılmalıdır","Gelişim sürekli olduğu için rehberlik hizmetleri de kesintisiz yapılmalıdır; gelişim bütün olduğu için birey bir bütün olarak ele alınmalıdır."],
    [1,"Aşağıdakilerden hangisi geleneksel rehberlik anlayışının özelliğidir?","Kriz ve sorun odaklı yardım hizmeti vardır","Gelişimi sağlayıcı ve kolaylaştırıcıdır","Tüm öğrencilere yöneliktir","Öğretmen odaklıdır","Öğretimle kaynaştırılmıştır","Geleneksel rehberlik kriz ve sorun odaklı, problemli öğrencilere yönelik, uzman odaklı ve tepkiseldir; diğer seçenekler gelişimsel rehberliğin özellikleridir."],
    [1,"Aşağıdakilerden hangisi geleneksel eğitim anlayışına özgüdür?","Ezbercilik önplandadır","Öğrenci aktiftir","Bireysel farklılıklara saygı esastır","Öğrenme yaşam boyu devam eder","Öğrenci merkezli anlayış hâkimdir","Geleneksel eğitimde konu ve öğretmen merkezlidir, ezbercilik önplandadır ve öğrenci pasiftir. Çağdaş eğitimde anlama, kavrama ve yapılandırma esastır."],

    [2,"Kapsamlı PDR programı MEB'de hangi eğitim döneminden itibaren uygulanmaya başlanmıştır?","2006-2007","1998-1999","2001-2002","2010-2011","2014-2015","Slayta göre kapsamlı PDR programı MEB'de 2006-2007 eğitim döneminden itibaren uygulanmaya başlanmıştır."],
    [2,"Kapsamlı PDR programı (K-12 rehberlik programı) hangi modele dayanır?","Gelişimsel rehberlik modeli","Parsons modeli","Klinik model","Eğitimle kaynaştırılmış model","Karar vermeye yardım süreci modeli","Program, gelişimsel yaklaşımın uygulamaya dönük yönünü oluşturur; öğrenci merkezlidir ve tüm öğrencilere yöneliktir."],
    [2,"Öğrencilerin kendi öğrenimlerini planlamalarına ve yönetmelerine yardımcı olan, psikolojik danışman tarafından planlanan etkinlikleri içeren boyut hangisidir?","Bireysel planlama","Rehberlik müfredatı","Müdahale hizmetleri","Sistem desteği","Disiplin hizmetleri","Bireysel planlama, öğrencilerin kişisel ve mesleki gelişimlerinin yanı sıra kendi öğrenimlerini planlamalarına ve yönetmelerine yardımcı olacak etkinlikleri içerir."],
    [2,"Öğrencilerin acil sorunlarına ve ihtiyaçlarına cevap vermeyi amaçlayan hizmetleri içeren boyut hangisidir?","Müdahale hizmetleri","Rehberlik müfredatı","Bireysel planlama","Sistem desteği","Araştırma-değerlendirme","Müdahale hizmetleri, öğrencilerin acil sorunlarına ve ihtiyaçlarına cevap vermeyi amaçlar."],
    [2,"PDR programının planlanması, hazırlanması, uygulanması, değerlendirilmesi ve geliştirilmesine yönelik yönetimsel ve eğitsel etkinlikleri kapsayan boyut hangisidir?","Sistem desteği","Rehberlik müfredatı","Bireysel planlama","Müdahale hizmetleri","Sevk hizmetleri","Sistem desteği, diğer üç boyutun desteklenmesi için gerekli program ve personel destekleme etkinliklerini içerir."],
    [2,"Kapsamlı PDR programında sınıf etkinliklerinin uygulanmasından kim sorumludur?","Sınıf rehber öğretmenleri","Okul müdürü","Yalnızca veliler","İlçe milli eğitim müdürü","Okul aile birliği","Programın içeriğindeki sınıf etkinliklerini sınıf rehber öğretmenleri yürütür; uzmanlık gerektiren uygulamalar psikolojik danışmanlar tarafından sağlanır."],
    [2,"Aşağıdakilerden hangisi ilk ve ortaöğretim kurumları sınıf rehberlik programında belirlenen yeterlik alanlarından biri DEĞİLDİR?","Fiziksel performans","Kendini kabul","Kişilerarası ilişkiler","Güvenli ve sağlıklı hayat","Toplum ve aile","Yedi yeterlik: okula ve çevreye uyum, kendini kabul, kişilerarası ilişkiler, eğitsel başarı, eğitsel ve mesleki gelişim, güvenli ve sağlıklı hayat, toplum ve aile."],
    [2,"Kapsamlı PDR programının temel ilkesi aşağıdakilerden hangisidir?","Bütün öğrencilerin gelişim görevlerini kazanmalarına ve gelişim krizlerini atlatmalarına yönelik önleyici etkinlikler sunmak","Yalnızca sorunlu öğrencileri iyileştirmek","Yalnızca sınav başarısını artırmak","Öğrencileri disiplin altına almak","Yalnızca meslek seçimine yardım etmek","Temel ilke, tüm öğrencilerin gelişim görevlerini kazanmalarına ve gelişim krizlerini atlatmalarına yönelik önleyici etkinlikler sunmaktır."],
    [2,"Kapsamlı PDR programıyla ilgili aşağıdakilerden hangisi doğrudur?","Etkinliklerin uygulama sırası ve yeterlik alanındaki değişimler psikolojik danışman onayı olmadan yapılamaz","Program, okul rehberlik ve psikolojik danışma programının tamamıdır","Etkinlik sayısı öğretim kademesi yükseldikçe azalır","Program hazırlanırken öncelikle psikolojik danışmanın rolü ve görevi dikkate alınır","Program katı ve değişmez bir yapıya sahiptir","Program ardışık ve esnek bir yapıya sahiptir; hazırlanırken içeriğe önem verilir; etkinlik sayısı öğretim kademesine göre artar; kapsamlı PDR programı okul rehberlik programının yalnızca bir parçasıdır."],

    [3,"İş ve İşçi Bulma Kurumu hangi hizmet alanındaki rehberliğe örnektir?","Endüstri alanında rehberlik","Eğitim alanında rehberlik","Sağlık alanında rehberlik","Sosyal yardım alanında rehberlik","Adalet ve güvenlik alanında rehberlik","Endüstri alanında rehberlik; sanayi kuruluşları, İş ve İşçi Bulma Kurumu ve sendikalar gibi yerlerde sürdürülür."],
    [3,"Okul öncesi (3-6 yaş) dönemde yürütülen rehberlik çalışmalarına aşağıdakilerden hangisi örnektir?","Okula uyum sağlama ve benlik kavramını güçlendirme","Meslek seçimine yöneltme","Burs, yurt, kredi bilgilendirmesi yapma","Karşı cinsi tanıma ve kabul etme","Üniversite tercih danışmanlığı","Okul öncesi rehberlik; okula uyum, benlik kavramının güçlendirilmesi, sosyalleşme ve gelişimsel, önleyici çalışmaları kapsar."],
    [3,"Ergenlik çağını kapsadığı için rehberlik hizmetlerine en çok ihtiyaç duyulan dönem aşağıdakilerden hangisidir?","Ortaöğretim dönemi","Okul öncesi dönem","İlköğretim birinci kademe","Yükseköğretim dönemi","Yetişkinlik dönemi","Slayta göre ortaöğretim dönemi ergenlik çağını kapsadığı için rehberlik hizmetlerine en çok ihtiyaç duyulan dönemdir; bu dönemde mesleki ve kişisel-sosyal rehberlik ön plandadır."],
    [3,"Okula yeni başlayan öğrencilere okulu ve okulun kurallarını tanıtmak hangi rehberlik türüne örnektir?","Uyum sağlayıcı rehberlik","Önleyici rehberlik","Yöneltici rehberlik","Tamamlayıcı rehberlik","Kriz müdahale rehberliği","Uyum sağlayıcı rehberlik, öğrencilerin eğitim-öğretim ortamlarına uyum sağlamalarını kolaylaştırır."],
    [3,"Meslek seçiminde kararsızlık yaşayan bir öğrenciye sunulacak rehberlik hizmeti hangi türdendir?","Yöneltici rehberlik","Uyum sağlayıcı rehberlik","Önleyici rehberlik","İyileştirici rehberlik","Tamamlayıcı rehberlik","Yöneltici rehberlik, bireyin ilgi, ihtiyaç ve yeteneklerine uygun meslek, okul veya programı seçmesi için yardım eder."],
    [3,"Sınıf öğretmeninin, öğrencilerin bireysel ve akademik başarılarını artırma konusunda rehberlik servisinden yardım alması hangi rehberlik türüne örnektir?","Tamamlayıcı rehberlik","Önleyici rehberlik","Yöneltici rehberlik","Kriz müdahale rehberliği","İyileştirici rehberlik","Tamamlayıcı rehberlik, eğitimin amaçlarının gerçekleşmesine yardımcı olmak için eğitim etkinlikleriyle birlikte bütünsel olarak verilir."],
    [3,"Öğrencileri ilgi, yetenek ve özelliklerine uygun eğitim programlarına yönlendiren ve eğitim planlamalarına yardım eden rehberlik hangisidir?","Ayarlayıcı rehberlik","Önleyici rehberlik","İyileştirici rehberlik","Kriz müdahale rehberliği","Uyum sağlayıcı rehberlik","Ayarlayıcı rehberlik, öğrencilerin eğitim programlarında yer almasında ve eğitim planlamalarında yol göstererek yardım eder."],
    [3,"Kriz müdahale (problem odaklı) rehberlik ile iyileştirici rehberlik arasındaki temel fark nedir?","Kriz müdahale olay/problem anında, iyileştirici ise olay/problem sonrasında yapılır","Kriz müdahale olaydan önce, iyileştirici olay anında yapılır","İkisi de olaydan önce yapılır","İkisi de yalnızca okul öncesinde yapılır","İyileştirici ciddi travmalara, kriz müdahale hafif sorunlara yöneliktir","Kriz yönelimli rehberlik olay/problem anında yapılan müdahaledir; iyileştirici rehberlik olay/problem sonrası yapılandır. Kriz ciddi travmalarla, iyileştirici ise sınav kaygısı, uyum sorunları gibi daha hafif sorunlarla ilgilenir."],
    [3,"Duyuşsal yönü ağır basan ve yalnızca psikolojik danışma uzmanları tarafından sunulan hizmet aşağıdakilerden hangisidir?","Psikolojik danışma","Rehberlik","Grup rehberliği","Sınıf rehberliği","Oryantasyon","Rehberlik bilişsel düzeyde ve bilgilendirme ağırlıklı yapılırken psikolojik danışmada duyuşsal yön ağır basar ve hizmeti yalnızca psikolojik danışma uzmanları sunar."],
    [3,"Grupla psikolojik danışmanın bireysel danışmaya göre üstün yönlerinden biri aşağıdakilerden hangisidir?","Birden fazla danışanın aynı anda yararlanması nedeniyle zaman yönünden daha ekonomiktir","Derinlemesine yardım verilebilir","Gizliliği sağlamak daha kolaydır","Ağır vakalara çözüm bulmak kolaylaşır","Baskın üyeler gruba zarar vermez","Grupla danışmada danışanlar sorunlarının yalnızca kendilerine özgü olmadığını görür, başkalarının çözüm yollarını öğrenir ve gruba ait olma duygusu yaşar; diğer seçenekler zayıf yönleridir."],

    [4,"Eğitsel rehberliğin temel amacı aşağıdakilerden hangisidir?","Öğrencinin “öğrenmeyi öğrenmesini” sağlamak","Öğrenciye hazır bilgi vermek","Öğrencinin sınav sonuçlarını yükseltmek","Öğrenciyi disipline etmek","Öğrenciyi bir mesleğe yerleştirmek","Eğitsel rehberliğin temel amacı öğrencinin öğrenmeyi öğrenmesini sağlamaktır: “çocuğa balık vermek değil, balık tutmayı öğretmektir”."],
    [4,"Slayta göre sınav kaygısı ile ilgili aşağıdakilerden hangisi doğrudur?","Önemli olan sınav kaygısını yok etmek değil, onunla yaşamayı öğrenmektir","Her düzeydeki kaygı öğrenmeyi olumlu etkiler","Aşırı kaygı öğrenmeyi artırır","Kaygı tamamen ortadan kaldırılmalıdır","Normal düzeydeki kaygı olumsuz sayılır","Öğrenme için normal düzeyde kaygı gereklidir; aşırı ve yetersiz kaygı olumsuz etki yapar."],
    [4,"Aşağıdakilerden hangisi sınav kaygısıyla başa çıkmada kullanılan bilinçli başa çıkma yollarından biri DEĞİLDİR?","Savunma mekanizmalarını kullanma","Gevşeme egzersizleri yapma","Zaman yönetimi","Verimli ders çalışma yöntemlerine göre çalışma","Sınavla ilgili yanlış inanç ve düşünceleri değiştirme","Savunma mekanizmaları bilinçsiz olarak kullanılan girişimlerdir; bilinçli başa çıkma yolları gevşeme, zihinsel düzenleme, yanlış inançları değiştirme, zaman yönetimi ve verimli çalışma gibi becerilerdir."],
    [4,"Akran danışmanlığı aşağıdakilerden hangisidir?","Üst sınıflardan nitelikli öğrencilerin eğitim alıp denetim altında diğer öğrencilere kişisel ve akademik konularda destek olması","Öğretmenlerin öğrencilere disiplin sağlaması","Velilerin okulda danışmanlık yapması","Psikolojik danışmanın aileleri yönlendirmesi","Öğrencilerin birbirini sınaması","Akran danışmanlığı, belirli bir eğitim gören ve bir süpervizör tarafından denetlenen öğrencilerin kendi yaşıtlarına ve alt sınıf öğrencilerine destek olma sürecidir."],

    [5,"Öğrenci kişilik hizmetlerinin (ÖKH) alanları hangi seçenekte doğru verilmiştir?","Sağlık, sosyal yardım, rehberlik, özel eğitim/özel yetiştirme, sosyal-kültürel hizmetler","Sağlık, disiplin, rehberlik, yönetim, sosyal-kültürel hizmetler","Rehberlik, ölçme, değerlendirme, sağlık, disiplin","Sosyal yardım, rehberlik, yönetim, öğretim, sağlık","Sağlık, öğretim, rehberlik, özel eğitim, disiplin","ÖKH beş alandan oluşur: I. Sağlık, II. Sosyal yardım, III. Rehberlik, IV. Özel eğitim/özel yetiştirme, V. Sosyal/kültürel hizmetler."],
    [5,"Aşağıdakilerden hangisi rehberliğin doğrudan hizmetlerinden biridir?","Bilgi toplama ve yayma","Araştırma-değerlendirme","Plan ve program hazırlama","Müşavirlik (konsültasyon)","Veli ile ilişkiler","Doğrudan hizmetler: bireyi tanıma, bilgi toplama ve yayma, yöneltme ve yerleştirme, oryantasyon, psikolojik danışma, sevk, izleme. Diğer seçenekler dolaylı hizmetlerdir."],
    [5,"Okulun ve okulda bulunan imkânların tanıtılması amacıyla, özellikle öğretim yılı başında okula yeni başlayan öğrencilere verilen hizmet hangisidir?","Oryantasyon","İzleme","Sevk","Müşavirlik","Araştırma-değerlendirme","Oryantasyon hizmetleri, öğrencilere okulu ve okulda bulunan imkânları tanıtma amacına yönelik çalışmaları kapsar."],
    [5,"Yöneltilen ve yerleştirilen öğrencilerin başarı ve uyum durumlarını inceleyen, rehberlik faaliyetlerinin etkililiğini ortaya koymak için bilgi sağlayan hizmet hangisidir?","İzleme","Sevk","Oryantasyon","Müşavirlik","Bireyi tanıma","İzleme, yöneltme ve yerleştirme sonucunda öğrencilerin başarı ve yaşadıkları uyum güçlüklerinin incelenmesidir; ayrıca rehberlik faaliyetlerinin etkililiği için gerekli bilgileri sağlar."],
    [5,"Psikolojik danışmanın yardım sağlayamayacağını fark ettiği öğrenciyi, yardım alabileceği kişi ya da kuruma yönlendirmesi hangi hizmete örnektir?","Sevk (refere)","İzleme","Oryantasyon","Bilgi toplama ve yayma","Yöneltme ve yerleştirme","Sevk (refere), okul psikolojik danışmanının kendisine gereken yardımı sağlayamayacağını fark ettiğinde öğrenciyi ya da ailesini yardım alabileceği kişi veya kuruma yönlendirmesidir."],
    [5,"Yönetici, öğretmen ve anne babaların rehberlik konusunda daha yeterli hale gelmesini ve işbirliği içinde çalışmalarını sağlamayı amaçlayan dolaylı hizmet hangisidir?","Konsültasyon (müşavirlik)","Sevk","İzleme","Oryantasyon","Bireyi tanıma","Konsültasyon, yönetici, öğretmen ve anne babaların rehberlik konusunda yeterli hale gelmesini ve işbirliği içinde çalışmalarını sağlar."]
  ];

  var $ = function (id) { return document.getElementById(id); };
  var Q = [], ans = {}, timerId = null, endAt = 0, startedAt = 0, name = '', finished = false, filter = 'all';

  function esc(s) { return String(s).replace(/[&<>"]/g, function (c) { return { '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;' }[c]; }); }
  function shuffle(a) { for (var i = a.length - 1; i > 0; i--) { var j = Math.floor(Math.random() * (i + 1)); var t = a[i]; a[i] = a[j]; a[j] = t; } return a; }
  function fmt(ms) { var s = Math.max(0, Math.ceil(ms / 1000)); return String(Math.floor(s / 60)).padStart(2, '0') + ':' + String(s % 60).padStart(2, '0'); }

  function buildQuestions() {
    Q = RAW.map(function (r, i) {
      var opts = shuffle([2, 3, 4, 5, 6].map(function (k) { return { t: r[k], c: k === 2 }; }));
      return { n: i + 1, topic: r[0], q: r[1], o: opts.map(function (x) { return x.t; }), a: opts.findIndex(function (x) { return x.c; }), e: r[7] };
    });
  }

  function buildExam() {
    $('questions').innerHTML = Q.map(function (q) {
      return '<article class="q" id="q' + q.n + '"><div class="qhead"><span class="qn">' + q.n + '</span><p class="qt">' + esc(q.q) + '</p></div>' +
        '<div class="opts" role="radiogroup" aria-label="Soru ' + q.n + '">' + q.o.map(function (o, i) {
          return '<label class="opt"><input type="radio" name="q' + q.n + '" value="' + i + '"><span class="ol">' + 'ABCDE'[i] + ')</span><span>' + esc(o) + '</span></label>';
        }).join('') + '</div></article>';
    }).join('');
    $('navgrid').innerHTML = Q.map(function (q) { return '<button type="button" data-go="' + q.n + '" id="nv' + q.n + '" aria-label="Soru ' + q.n + '">' + q.n + '</button>'; }).join('');
    refreshProgress();
  }

  function answeredCount() { return Object.keys(ans).length; }
  function refreshProgress() {
    var c = answeredCount();
    $('progText').textContent = c + ' / ' + Q.length + ' cevaplandı';
    $('progBar').style.width = (c / Q.length * 100) + '%';
    $('leftText').textContent = (Q.length - c) > 0 ? (Q.length - c) + ' soru boş' : 'Tüm sorular cevaplandı';
    Q.forEach(function (q) { var b = $('nv' + q.n); if (b) b.classList.toggle('done', ans[q.n] !== undefined); });
  }

  function tick() {
    var left = endAt - Date.now();
    $('timer').textContent = fmt(left);
    $('timer').classList.toggle('low', left <= 5 * 60 * 1000);
    if (left <= 0) finish();
  }

  function start() {
    name = $('studentName').value.trim();
    ans = {}; finished = false; filter = 'all';
    buildQuestions(); buildExam();
    $('intro').hidden = true; $('result').hidden = true; $('exam').hidden = false;
    startedAt = Date.now(); endAt = startedAt + DURATION;
    clearInterval(timerId); timerId = setInterval(tick, 500); tick();
    window.scrollTo(0, 0);
  }

  function askFinish() {
    var left = Q.length - answeredCount();
    $('confirmText').textContent = left > 0 ? left + ' soru boş. Testi bitirmek istiyor musun?' : 'Tüm soruları cevapladın. Testi bitirmek istiyor musun?';
    $('confirm').hidden = false;
  }

  function status(q) { var v = ans[q.n]; return v === undefined ? 'blank' : (Number(v) === q.a ? 'ok' : 'no'); }

  function finish() {
    if (finished) return;
    finished = true; clearInterval(timerId); $('confirm').hidden = true;
    var used = Math.min(DURATION, Date.now() - startedAt);
    $('exam').hidden = true;
    renderResult(used);
    $('result').hidden = false;
    window.scrollTo(0, 0);
  }

  function reviewItem(q) {
    var st = status(q), v = ans[q.n];
    var pill = st === 'ok' ? '<span class="pill ok">Doğru · +' + PTS + '</span>' : st === 'no' ? '<span class="pill no">Yanlış · 0</span>' : '<span class="pill blank">Boş · 0</span>';
    return '<article class="rv" data-st="' + st + '"><span class="topic">' + TOPICS[q.topic] + '</span>' +
      '<div class="rvhead"><span class="qn">' + q.n + '</span><p class="qt">' + esc(q.q) + '</p>' + pill + '</div>' +
      '<ul class="ropts">' + q.o.map(function (o, i) {
        var picked = v !== undefined && Number(v) === i;
        var cls = i === q.a ? 'ok' : (picked ? 'no' : '');
        var tag = i === q.a ? (picked ? 'Senin cevabın · doğru' : 'Doğru cevap') : (picked ? 'Senin cevabın' : '');
        return '<li class="' + cls + '"><span><span class="mono">' + 'ABCDE'[i] + ')</span> ' + esc(o) + '</span>' + (tag ? '<span class="tag">' + tag + '</span>' : '') + '</li>';
      }).join('') + '</ul><p class="exp">' + esc(q.e) + '</p></article>';
  }

  function renderResult(used) {
    var ok = 0, no = 0, blank = 0, byTopic = TOPICS.map(function () { return { ok: 0, n: 0 }; });
    Q.forEach(function (q) { var s = status(q); if (s === 'ok') ok++; else if (s === 'no') no++; else blank++; byTopic[q.topic].n++; if (s === 'ok') byTopic[q.topic].ok++; });
    var score = ok * PTS;
    var h = '<div class="wrap"><div class="sheet"><div><p class="eyebrow">Test sonucu' + (name ? ' · ' + esc(name) : '') + '</p><h1>Rehberlik ve Psikolojik Danışma</h1></div>' +
      '<div class="total"><span class="big">' + score + '</span><span>/ 100 puan · kullanılan süre <span class="mono">' + fmt(used) + '</span></span></div>' +
      '<div class="track"><i style="width:' + score + '%"></i></div>' +
      '<div class="counts"><div class="g"><b>' + ok + '</b><span>Doğru</span></div><div class="r"><b>' + no + '</b><span>Yanlış</span></div><div class="y"><b>' + blank + '</b><span>Boş</span></div></div>' +
      '<div class="table-scroll"><table><thead><tr><th>Konu</th><th class="num">Doğru</th><th>Başarı</th></tr></thead><tbody>' +
      TOPICS.map(function (t, i) { var b = byTopic[i], p = Math.round(b.ok / b.n * 100); return '<tr><td>' + t + '</td><td class="num">' + b.ok + ' / ' + b.n + '</td><td><div class="minibar" role="img" aria-label="%' + p + '"><i style="width:' + p + '%"></i></div></td></tr>'; }).join('') +
      '</tbody></table></div>' +
      '<div><button class="btn" id="retryBtn" type="button">Testi yeniden çöz</button></div></div>' +
      '<div class="filters" id="filters" role="group" aria-label="Soruları süz">' +
      '<button type="button" data-f="all" aria-pressed="true">Tümü (' + Q.length + ')</button>' +
      '<button type="button" data-f="no" aria-pressed="false">Yanlışlar (' + no + ')</button>' +
      '<button type="button" data-f="blank" aria-pressed="false">Boşlar (' + blank + ')</button></div>' +
      '<div id="review" class="wrap">' + Q.map(reviewItem).join('') + '</div></div>';
    $('result').innerHTML = h;
  }

  function applyFilter(f) {
    filter = f;
    var shown = 0;
    document.querySelectorAll('#review .rv').forEach(function (el) {
      var show = f === 'all' || el.getAttribute('data-st') === f;
      el.hidden = !show; if (show) shown++;
    });
    document.querySelectorAll('#filters button').forEach(function (b) { b.setAttribute('aria-pressed', b.getAttribute('data-f') === f ? 'true' : 'false'); });
    var old = $('emptyMsg'); if (old) old.remove();
    if (!shown) { var p = document.createElement('p'); p.className = 'empty'; p.id = 'emptyMsg'; p.textContent = 'Bu süzgece uyan soru yok.'; $('review').appendChild(p); }
  }

  $('startBtn').addEventListener('click', start);
  $('finishTop').addEventListener('click', askFinish);
  $('finishBottom').addEventListener('click', askFinish);
  $('confirmNo').addEventListener('click', function () { $('confirm').hidden = true; });
  $('confirmYes').addEventListener('click', finish);
  $('navgrid').addEventListener('click', function (e) {
    var b = e.target.closest('[data-go]'); if (!b) return;
    var el = $('q' + b.getAttribute('data-go'));
    if (el) el.scrollIntoView({ behavior: window.matchMedia('(prefers-reduced-motion: reduce)').matches ? 'auto' : 'smooth', block: 'start' });
  });
  $('questions').addEventListener('change', function (e) {
    var t = e.target; if (t.type !== 'radio') return;
    var n = Number(t.name.slice(1));
    ans[n] = t.value;
    $('questions').querySelectorAll('input[name="q' + n + '"]').forEach(function (r) { r.closest('.opt').classList.toggle('sel', r.checked); });
    refreshProgress();
  });
  $('result').addEventListener('click', function (e) {
    var f = e.target.closest('[data-f]');
    if (f) { applyFilter(f.getAttribute('data-f')); return; }
    if (e.target.id === 'retryBtn') { $('result').hidden = true; $('intro').hidden = false; window.scrollTo(0, 0); }
  });
})();
</script>

</body></html>
