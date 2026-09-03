<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>NDABA — Réseau social du Wakanda</title>
<!-- Aperçu de lien. Ces balises ne s'appliquent QUE si le fichier est
     hébergé sur votre propre domaine : sur claude.ai, l'aperçu est
     produit par la page d'Anthropic, pas par ce document.
     Remplacez l'URL de og:image par celle de votre visuel. -->
<meta property="og:type" content="website">
<meta property="og:site_name" content="NDABA">
<meta property="og:title" content="NDABA — Réseau social du Wakanda">
<meta property="og:description" content="Le réseau social du royaume. Créez votre compte, publiez, suivez les autres agents.">
<meta property="og:image" content="https://exemple.com/ndaba-preview.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta name="twitter:card" content="summary_large_image">
<meta name="theme-color" content="#08060c">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;600;700&family=Rajdhani:wght@400;500;600;700&family=Work+Sans:wght@300;400;500;600&family=Space+Mono:wght@400;700&display=swap">
<style>
:root{
  --void:#08060c;--void2:#0e0a16;--surf:#151022;--surf2:#1d1630;
  --line:#2b2140;--line2:#3d2f5a;
  --i0:#f4efff;--i1:#cfc4e4;--i2:#9c8fba;--i3:#6b6088;
  --vib:#a865e8;--vib2:#7a4fae;--vibg:#cba4f5;
  --gold:#e0ab48;--goldg:#f6d18a;
  --tur:#2fa8a0;--turg:#68e0d6;
  --red:#c0503a;--redg:#e8846c;
  --fd:'Cinzel',serif;--fu:'Rajdhani',sans-serif;--fb:'Work Sans',sans-serif;--fm:'Space Mono',monospace;
  --ez:cubic-bezier(.22,.85,.32,1);--ezo:cubic-bezier(.16,1,.3,1);
}
*,*::before,*::after{box-sizing:border-box;}
html{color-scheme:dark;}
body{margin:0;background:var(--void);color:var(--i1);font-family:var(--fb);font-size:15px;line-height:1.55;min-height:100vh;overflow-x:hidden;-webkit-font-smoothing:antialiased;}
body::before{content:'';position:fixed;inset:0;z-index:-3;
  background:radial-gradient(ellipse 800px 560px at 50% 0%,rgba(168,101,232,.16),transparent 62%),
             radial-gradient(ellipse 700px 500px at 88% 88%,rgba(47,168,160,.09),transparent 62%),
             radial-gradient(ellipse 600px 460px at 6% 76%,rgba(224,171,72,.07),transparent 62%);}
body::after{content:'';position:fixed;inset:0;z-index:-1;pointer-events:none;opacity:.4;
  background-image:linear-gradient(135deg,rgba(168,101,232,.05) 25%,transparent 25.5%),
                   linear-gradient(225deg,rgba(168,101,232,.05) 25%,transparent 25.5%);
  background-size:32px 24px;}
#dust{position:fixed;inset:0;z-index:-2;pointer-events:none;}
h1,h2,h3{font-family:var(--fd);color:var(--i0);margin:0;font-weight:600;letter-spacing:.02em;}
p{margin:0 0 .9em;}p:last-child{margin:0;}
::selection{background:var(--vib2);color:#fff;}
button,input,textarea,select{font:inherit;}
img{display:block;max-width:100%;}
.mono{font-family:var(--fm);}
.eyebrow{font-family:var(--fu);text-transform:uppercase;letter-spacing:.18em;font-size:10px;font-weight:600;color:var(--vibg);}
.gw{display:inline-flex;gap:.14em;vertical-align:middle;}
.gw svg{height:1em;width:auto;overflow:visible;}
.hex{clip-path:polygon(0 14px,14px 0,calc(100% - 14px) 0,100% 14px,100% calc(100% - 14px),calc(100% - 14px) 100%,14px 100%,0 calc(100% - 14px));}

/* ---------- chargement ---------- */
/* ==================== OUVERTURE ====================
   Le réseau ne « charge » pas : il s'allume. Un point de vibranium
   s'amorce, la trame hexagonale fleurit vers l'extérieur, les
   filaments relient les nœuds, l'emblème se reconstitue de ses
   éclats, puis l'onde de choc ouvre l'interface. */
#boot{position:fixed;inset:0;z-index:900;background:#020205;display:flex;flex-direction:column;
  align-items:center;justify-content:center;gap:14px;cursor:pointer;overflow:hidden;
  transition:opacity .9s var(--ez),visibility .9s;}
#boot::before{content:'';position:absolute;inset:0;
  background:radial-gradient(circle at 50% 46%,rgba(168,101,232,.20),transparent 46%),
             radial-gradient(circle at 50% 46%,rgba(47,168,160,.10),transparent 62%);
  opacity:0;animation:bglow 2.6s var(--ezo) .25s forwards;}
@keyframes bglow{to{opacity:1;}}
.bstage{position:relative;width:min(340px,76vw);aspect-ratio:1;display:flex;align-items:center;justify-content:center;}
.bstage>svg{position:absolute;inset:0;width:100%;height:100%;overflow:visible;pointer-events:none;}
/* Seul l'emblème reste cliquable : les autres couches, notamment les
   ondes de choc figées à leur pleine extension, recouvriraient le
   centre et absorberaient le geste. */
.bstage .bwave,.bstage .bcore,.bstage .bgrid,.bstage .bfil,.bstage .brib,.bstage .bglyphs{pointer-events:none;}
.blogo{pointer-events:auto;z-index:4;}
.blogo .bhit{pointer-events:none;}
#boot.ready .blogo .bhit{pointer-events:auto;cursor:pointer;}

/* noyau qui s'amorce */
.bcore{position:absolute;width:8px;height:8px;border-radius:50%;background:#fff;
  box-shadow:0 0 0 0 rgba(203,164,245,.9);opacity:0;animation:coreIgn 1.5s var(--ezo) .1s forwards;}
@keyframes coreIgn{
  0%{opacity:0;transform:scale(.2);box-shadow:0 0 0 0 rgba(203,164,245,0);}
  22%{opacity:1;transform:scale(1.9);box-shadow:0 0 34px 12px rgba(203,164,245,.85);}
  60%{opacity:1;transform:scale(1);box-shadow:0 0 22px 6px rgba(168,101,232,.6);}
  100%{opacity:.5;transform:scale(.7);box-shadow:0 0 16px 3px rgba(168,101,232,.35);}
}

/* trame hexagonale en floraison */
.bgrid polygon{fill:none;stroke:rgba(168,101,232,.5);stroke-width:.9;opacity:0;transform-box:fill-box;transform-origin:center;
  animation:hexBloom 1.5s var(--ezo) both;}
@keyframes hexBloom{
  0%{opacity:0;transform:scale(.1) rotate(-40deg);}
  45%{opacity:1;stroke:rgba(203,164,245,.95);}
  100%{opacity:.36;transform:none;}
}

/* filaments d'énergie */
.bfil line{stroke:rgba(104,224,214,.75);stroke-width:.7;stroke-linecap:round;
  stroke-dasharray:200;stroke-dashoffset:200;animation:filDraw .9s var(--ezo) both;
  filter:drop-shadow(0 0 4px rgba(104,224,214,.9));}
@keyframes filDraw{60%{stroke-dashoffset:0;opacity:1;}100%{stroke-dashoffset:0;opacity:.35;}}

/* glyphes en orbite */
.bglyphs{animation:orbit 26s linear infinite;}
@keyframes orbit{to{transform:rotate(360deg);}}
.bglyphs g{opacity:0;animation:glyphFade 1.1s var(--ezo) both;}
@keyframes glyphFade{to{opacity:.5;}}
.bglyphs path{fill:rgba(246,209,138,.75);}

/* emblème reconstitué */
.blogo{filter:drop-shadow(0 0 20px rgba(168,101,232,.75));}
.blogo .frag{fill:rgba(168,101,232,.16);stroke:var(--vibg);stroke-width:1.6;opacity:0;
  transform-box:fill-box;transform-origin:50px 50px;animation:fragIn 1.1s var(--ezo) both;}
@keyframes fragIn{
  0%{opacity:0;transform:translate(var(--fx),var(--fy)) rotate(var(--fr)) scale(.4);}
  70%{opacity:1;}
  100%{opacity:1;transform:none;}
}
.blogo .bhub{fill:var(--vibg);opacity:0;animation:hubIn .8s var(--ezo) 1.5s both;}
@keyframes hubIn{0%{opacity:0;transform-box:fill-box;transform-origin:center;transform:scale(0);}
  60%{opacity:1;transform:scale(1.4);}100%{opacity:1;transform:scale(1);}}
.blogo .barc{fill:none;stroke:var(--turg);stroke-width:1.2;opacity:.85;
  stroke-dasharray:251;stroke-dashoffset:251;transform-box:fill-box;transform-origin:center;transform:rotate(-90deg);
  animation:arcFill 2.4s var(--ez) .5s both;filter:drop-shadow(0 0 6px rgba(104,224,214,.8));}
@keyframes arcFill{to{stroke-dashoffset:0;}}

/* ondes de choc */
.bwave{position:absolute;width:60px;height:60px;border-radius:50%;border:1.5px solid rgba(203,164,245,.85);pointer-events:none;
  opacity:0;animation:shock 1.5s var(--ezo) 2.5s forwards;}
.bwave.w2{animation-delay:2.72s;border-color:rgba(104,224,214,.7);}
@keyframes shock{0%{opacity:.9;transform:scale(.3);}100%{opacity:0;transform:scale(7);}}

/* titre : glyphes qui basculent en lettres */
.bt{font-family:var(--fd);font-size:clamp(24px,6vw,40px);letter-spacing:.3em;color:var(--i0);display:flex;gap:.06em;
  text-shadow:0 0 40px rgba(203,164,245,.7);min-height:1.3em;align-items:center;}
.bt .ch{display:inline-flex;align-items:center;justify-content:center;width:1em;opacity:0;
  animation:chIn .5s var(--ezo) both;color:var(--vibg);}
.bt .ch svg{width:.78em;height:.78em;}
@keyframes chIn{0%{opacity:0;transform:translateY(16px) rotateX(70deg);filter:blur(6px);}
  100%{opacity:1;transform:none;filter:none;}}
.bt .ch.lock{color:var(--i0);animation:chFlip .5s var(--ezo) both;}
@keyframes chFlip{0%{transform:rotateX(90deg) scale(1.3);filter:blur(4px);}
  60%{transform:rotateX(-12deg) scale(1.06);}100%{transform:none;filter:none;}}
.bs{font-family:var(--fm);font-size:11px;color:var(--turg);letter-spacing:.12em;opacity:0;
  animation:chIn .8s var(--ezo) 2.3s both;}
.bskip{font-family:var(--fu);font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:var(--i3);
  opacity:0;animation:blink 2.6s ease-in-out 3.1s infinite;}
@keyframes blink{0%,100%{opacity:.25;}50%{opacity:.7;}}
.bflash{position:absolute;inset:0;background:radial-gradient(circle at 50% 46%,#fff,rgba(203,164,245,.7) 30%,transparent 62%);
  opacity:0;pointer-events:none;}
.bflash.go{animation:flash .85s var(--ez) forwards;}
@keyframes flash{0%{opacity:0;}18%{opacity:.92;}100%{opacity:0;}}
/* emblème : devient une porte une fois la séquence refermée */
.blogo{cursor:default;transition:transform .5s var(--ez),filter .5s var(--ez);}
.blogo .bhalo{fill:none;stroke:var(--vibg);stroke-width:.8;opacity:0;transform-box:fill-box;transform-origin:center;}
#boot.ready .blogo{cursor:pointer;}
#boot.ready .blogo .bhalo{animation:haloRing 2.4s var(--ezo) infinite;}
@keyframes haloRing{0%{opacity:.75;transform:scale(.86);}70%{opacity:0;transform:scale(1.28);}100%{opacity:0;}}
#boot.ready .blogo{animation:doorBreathe 3.2s ease-in-out infinite;}
@keyframes doorBreathe{50%{transform:scale(1.035);filter:drop-shadow(0 0 44px rgba(203,164,245,.95));}}
#boot.ready .blogo:hover{transform:scale(1.09);filter:drop-shadow(0 0 60px rgba(203,164,245,1));animation:none;}
#boot.ready .blogo:active{transform:scale(.96);}

/* nom du réseau, révélé une fois les couches refermées */
.bname{display:flex;flex-direction:column;align-items:center;gap:2px;opacity:0;pointer-events:none;}
#boot.ready .bname{animation:nameIn 1s var(--ezo) forwards;}
@keyframes nameIn{0%{opacity:0;transform:translateY(20px);filter:blur(12px);letter-spacing:.9em;}
  100%{opacity:1;transform:none;filter:none;}}
.bname .l1{font-family:var(--fd);font-size:clamp(19px,4.4vw,27px);letter-spacing:.42em;color:var(--i0);
  text-indent:.42em;text-shadow:0 0 34px rgba(203,164,245,.8);}
.bname .l2{font-family:var(--fu);font-size:clamp(10px,2.4vw,13px);letter-spacing:.55em;text-transform:uppercase;
  color:var(--turg);text-indent:.55em;}
.bskip{opacity:0 !important;}
#boot.ready .bskip{animation:blink 2.6s ease-in-out .8s infinite !important;}

/* particules aspirées vers le noyau */
#bpart{position:absolute;inset:0;width:100%;height:100%;pointer-events:none;}

/* rubans d'énergie */
.brib path{fill:none;stroke-width:1.1;stroke-linecap:round;stroke-dasharray:520;stroke-dashoffset:520;
  animation:ribDraw 2.6s var(--ezo) both;filter:drop-shadow(0 0 6px currentColor);}
@keyframes ribDraw{
  0%{stroke-dashoffset:520;opacity:0;}
  25%{opacity:.9;}
  70%{stroke-dashoffset:0;opacity:.7;}
  100%{stroke-dashoffset:-140;opacity:.22;}
}

/* bouton de son */
.bsnd{position:absolute;top:calc(18px + env(safe-area-inset-top));right:18px;width:38px;height:38px;
  background:transparent;border:none;color:var(--i3);cursor:pointer;z-index:5;
  box-shadow:inset 0 0 0 1px rgba(168,101,232,.3);transition:all .3s var(--ez);
  clip-path:polygon(0 8px,8px 0,100% 0,100% calc(100% - 8px),calc(100% - 8px) 100%,0 100%);}
.bsnd svg{width:18px;height:18px;margin:auto;display:block;}
.bsnd:hover{color:var(--vibg);box-shadow:inset 0 0 0 1px var(--vibg);}
.bsnd.off{color:#4a4060;}
.bsnd.off::after{content:'';position:absolute;left:8px;right:8px;top:50%;height:1.5px;background:currentColor;transform:rotate(-38deg);}
.bsnd.pending{animation:sndPulse 1.6s ease-in-out infinite;color:var(--turg);box-shadow:inset 0 0 0 1px var(--turg);}
@keyframes sndPulse{50%{box-shadow:inset 0 0 0 1px var(--turg),0 0 18px -4px rgba(104,224,214,.9);}}

/* floraison de l'emblème, calée sur la frappe sonore */
@keyframes bloom{0%{filter:drop-shadow(0 0 18px rgba(168,101,232,.7));}
  40%{filter:drop-shadow(0 0 60px rgba(203,164,245,1)) brightness(1.5);}
  100%{filter:drop-shadow(0 0 22px rgba(168,101,232,.8));}}
.blogo.bloom{animation:bloom 1.1s var(--ezo);}

/* ouverture en iris : l'interface se dévoile par expansion circulaire */
.biris{position:absolute;inset:0;pointer-events:none;background:#020205;opacity:0;
  clip-path:circle(0% at 50% 46%);}
.biris.go{animation:iris 1s var(--ezo) forwards;}
@keyframes iris{
  0%{opacity:1;clip-path:circle(150% at 50% 46%);}
  100%{opacity:1;clip-path:circle(0% at 50% 46%);}
}
/* la scène recule et se dissout pendant l'ouverture */
#boot.gone .bstage{animation:stageOut .9s var(--ez) forwards;}
@keyframes stageOut{to{transform:scale(1.6) translateZ(0);opacity:0;filter:blur(18px);}}
#boot.gone .bt,#boot.gone .bs,#boot.gone .bskip{animation:txtOut .55s var(--ez) forwards;}
@keyframes txtOut{to{opacity:0;transform:translateY(-18px);filter:blur(10px);}}
#boot.gone{opacity:0;visibility:hidden;pointer-events:none;transition:opacity 1s var(--ez) .25s,visibility 1s .25s;}

/* l'application arrive en douceur derrière */
@keyframes appIn{from{opacity:0;transform:scale(1.03);filter:blur(10px);}to{opacity:1;transform:none;filter:none;}}
#app.arriving{animation:appIn 1s var(--ezo);}

/* ---------- coque ---------- */
.top{position:sticky;top:0;z-index:120;display:flex;align-items:center;justify-content:space-between;gap:12px;
  padding:11px 16px;background:linear-gradient(180deg,rgba(14,10,22,.95),rgba(8,6,12,.7));backdrop-filter:blur(14px);
  border-bottom:1px solid rgba(168,101,232,.22);}
.top .lg{display:flex;align-items:center;gap:9px;cursor:pointer;}
.top .lg svg{width:24px;height:24px;color:var(--vibg);filter:drop-shadow(0 0 7px rgba(168,101,232,.6));}
.top .lg .n{font-family:var(--fd);font-size:16px;letter-spacing:.16em;color:var(--i0);}
.top .rt{display:flex;align-items:center;gap:8px;}
.ib{width:34px;height:34px;display:flex;align-items:center;justify-content:center;background:transparent;border:none;
  color:var(--i2);cursor:pointer;box-shadow:inset 0 0 0 1px var(--line);transition:all .2s;
  clip-path:polygon(0 7px,7px 0,100% 0,100% calc(100% - 7px),calc(100% - 7px) 100%,0 100%);position:relative;}
.ib:hover,.ib.on{color:var(--vibg);box-shadow:inset 0 0 0 1px var(--vib2);}
.ib svg{width:17px;height:17px;}
.ib .badge{position:absolute;top:-4px;right:-4px;min-width:15px;height:15px;padding:0 4px;font-family:var(--fm);font-size:9px;
  color:#140a1e;background:var(--vibg);display:flex;align-items:center;justify-content:center;}
main{max-width:620px;margin:0 auto;padding:16px 14px 92px;}
.nav{position:fixed;left:0;right:0;bottom:0;z-index:120;display:flex;justify-content:center;gap:4px;
  padding:9px 12px;background:linear-gradient(0deg,rgba(14,10,22,.96),rgba(8,6,12,.7));backdrop-filter:blur(14px);
  border-top:1px solid rgba(168,101,232,.22);}
.nav button{flex:1;max-width:96px;padding:9px 6px;display:flex;flex-direction:column;align-items:center;gap:3px;
  background:transparent;border:none;color:var(--i3);cursor:pointer;transition:all .2s;font-family:var(--fu);font-size:9.5px;
  letter-spacing:.09em;text-transform:uppercase;}
.nav button svg{width:19px;height:19px;}
.nav button.on{color:var(--vibg);}
.nav button.on svg{filter:drop-shadow(0 0 8px rgba(168,101,232,.8));}

/* ---------- composants ---------- */
.card{background:linear-gradient(158deg,rgba(29,22,48,.62),rgba(8,6,12,.86));backdrop-filter:blur(6px);
  box-shadow:inset 0 0 0 1px rgba(168,101,232,.2);margin-bottom:16px;
  clip-path:polygon(0 15px,15px 0,calc(100% - 15px) 0,100% 15px,100% calc(100% - 15px),calc(100% - 15px) 100%,15px 100%,0 calc(100% - 15px));}
.btn{padding:10px 17px;font-family:var(--fu);font-size:11.5px;letter-spacing:.1em;text-transform:uppercase;font-weight:600;
  color:var(--vibg);background:linear-gradient(160deg,rgba(168,101,232,.12),transparent);border:none;cursor:pointer;
  box-shadow:inset 0 0 0 1px var(--vib2);transition:all .2s;
  clip-path:polygon(0 8px,8px 0,100% 0,100% calc(100% - 8px),calc(100% - 8px) 100%,0 100%);}
.btn:hover:not(:disabled){background:rgba(168,101,232,.22);box-shadow:inset 0 0 0 1px var(--vibg),0 0 18px -5px rgba(168,101,232,.7);}
.btn:disabled{opacity:.34;cursor:not-allowed;}
.btn.sm{padding:7px 12px;font-size:10.5px;}
.btn.gold{color:var(--goldg);box-shadow:inset 0 0 0 1px rgba(224,171,72,.5);}
.btn.gold:hover:not(:disabled){background:rgba(224,171,72,.18);}
.btn.ghost{color:var(--i2);box-shadow:inset 0 0 0 1px var(--line);}
.btn.ghost:hover{color:var(--i0);}
.inp,.txa,.sel{width:100%;padding:10px 13px;border:none;outline:none;color:var(--i0);font-family:var(--fb);font-size:14px;
  background:linear-gradient(158deg,rgba(29,22,48,.7),rgba(8,6,12,.88));box-shadow:inset 0 0 0 1px var(--line);
  clip-path:polygon(0 8px,8px 0,100% 0,100% calc(100% - 8px),calc(100% - 8px) 100%,0 100%);}
.inp:focus,.txa:focus{box-shadow:inset 0 0 0 1px var(--vib);}
.txa{min-height:78px;resize:vertical;}
.lbl{font-family:var(--fu);font-size:9.5px;letter-spacing:.13em;text-transform:uppercase;color:var(--i3);margin-bottom:5px;display:block;}
.av{border-radius:50%;overflow:hidden;background:linear-gradient(158deg,var(--surf2),var(--void2));flex:none;position:relative;
  box-shadow:inset 0 0 0 1px rgba(168,101,232,.35);}
.av img{width:100%;height:100%;object-fit:cover;}
.av .ph{width:100%;height:100%;display:flex;align-items:center;justify-content:center;color:var(--i3);font-family:var(--fd);font-size:.9em;}
.ring{padding:2px;border-radius:50%;background:conic-gradient(from 0deg,var(--vibg),var(--turg),var(--goldg),var(--vibg));}
.ring.seen{background:var(--line);}

/* stories */
.stories{display:flex;gap:12px;overflow-x:auto;padding:4px 2px 12px;margin-bottom:6px;}
.stories::-webkit-scrollbar{height:0;}
.st{display:flex;flex-direction:column;align-items:center;gap:5px;cursor:pointer;flex:none;width:66px;}
.st .h{font-family:var(--fu);font-size:10px;color:var(--i2);max-width:66px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.st .av{width:58px;height:58px;}

/* publication */
.post-h{display:flex;align-items:center;gap:10px;padding:12px 14px;}
.post-h .av{width:38px;height:38px;cursor:pointer;}
.post-h .nm{font-family:var(--fu);font-size:14px;font-weight:600;color:var(--i0);letter-spacing:.03em;cursor:pointer;}
.post-h .sub{font-family:var(--fm);font-size:10px;color:var(--i3);}
.media{position:relative;background:#05040a;aspect-ratio:1;overflow:hidden;}
.media .slides{display:flex;height:100%;transition:transform .4s var(--ez);}
.media .sl{min-width:100%;height:100%;position:relative;}
.media img,.media video{width:100%;height:100%;object-fit:cover;}
.media .nav-a{position:absolute;top:50%;transform:translateY(-50%);width:30px;height:30px;background:rgba(8,6,12,.6);
  border:none;color:var(--i0);cursor:pointer;backdrop-filter:blur(4px);box-shadow:inset 0 0 0 1px rgba(203,164,245,.3);}
.media .nav-a.l{left:8px;}.media .nav-a.r{right:8px;}
.media .dots{position:absolute;bottom:9px;left:50%;transform:translateX(-50%);display:flex;gap:5px;}
.media .dots i{width:5px;height:5px;border-radius:50%;background:rgba(244,239,255,.35);}
.media .dots i.on{background:var(--vibg);box-shadow:0 0 7px var(--vibg);}
.media .cnt{position:absolute;top:10px;right:10px;font-family:var(--fm);font-size:10.5px;color:var(--i0);
  background:rgba(8,6,12,.6);padding:3px 8px;backdrop-filter:blur(4px);}
.acts{display:flex;align-items:center;gap:6px;padding:10px 12px 6px;}
.acts button{background:transparent;border:none;color:var(--i2);cursor:pointer;padding:5px;display:flex;align-items:center;gap:5px;
  font-family:var(--fm);font-size:12px;transition:all .2s;}
.acts button:hover{color:var(--i0);}
.acts button svg{width:21px;height:21px;}
.acts button.liked{color:var(--redg);}
.acts button.liked svg{fill:var(--redg);filter:drop-shadow(0 0 8px rgba(232,132,108,.7));}
.acts .sp{flex:1;}
.pbody{padding:0 14px 13px;}
.pbody .likes{font-family:var(--fu);font-size:13px;color:var(--i0);font-weight:600;letter-spacing:.03em;}
.pbody .cap{font-size:14px;color:var(--i1);margin-top:5px;}
.pbody .cap b{color:var(--i0);font-family:var(--fu);font-weight:600;}
.pbody .cmts{margin-top:8px;font-size:13.5px;color:var(--i2);cursor:pointer;}
.pbody .time{font-family:var(--fm);font-size:9.5px;color:var(--i3);margin-top:8px;letter-spacing:.05em;text-transform:uppercase;}

/* profil */
.phead{display:flex;gap:18px;align-items:center;padding:18px 14px;}
.phead .av{width:84px;height:84px;}
.stats{display:flex;gap:20px;flex:1;flex-wrap:wrap;}
.stat{text-align:center;cursor:pointer;}
.stat .n{font-family:var(--fm);font-size:17px;color:var(--i0);}
.stat .l{font-family:var(--fu);font-size:9.5px;letter-spacing:.1em;text-transform:uppercase;color:var(--i3);}
.pbio{padding:0 14px 14px;}
.pbio .nm{font-family:var(--fu);font-size:15px;font-weight:600;color:var(--i0);}
.pbio .bio{font-size:13.5px;color:var(--i1);margin-top:3px;white-space:pre-wrap;}
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:3px;}
.gcell{aspect-ratio:1;position:relative;overflow:hidden;cursor:pointer;background:#05040a;}
.gcell img,.gcell video{width:100%;height:100%;object-fit:cover;transition:transform .35s var(--ez);}
.gcell:hover img{transform:scale(1.06);}
.gcell .multi{position:absolute;top:6px;right:6px;color:#fff;filter:drop-shadow(0 1px 3px rgba(0,0,0,.8));}
.gcell .multi svg{width:15px;height:15px;}
.hls{display:flex;gap:14px;overflow-x:auto;padding:6px 14px 16px;}
.hl{display:flex;flex-direction:column;align-items:center;gap:5px;cursor:pointer;flex:none;width:64px;}
.hl .av{width:56px;height:56px;}
.hl .t{font-family:var(--fu);font-size:10px;color:var(--i2);max-width:64px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}

/* recherche & listes */
.urow{display:flex;align-items:center;gap:12px;padding:11px 13px;cursor:pointer;transition:background .2s;}
.urow:hover{background:rgba(168,101,232,.07);}
.urow .av{width:44px;height:44px;}
.urow .bd{flex:1;min-width:0;}
.urow .h{font-family:var(--fu);font-size:14px;font-weight:600;color:var(--i0);}
.urow .s{font-size:12.5px;color:var(--i3);overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}

/* messages */
.thread{display:flex;flex-direction:column;gap:8px;padding:14px;max-height:52vh;overflow-y:auto;}
.msg{max-width:78%;padding:9px 13px;font-size:14px;
  clip-path:polygon(0 9px,9px 0,100% 0,100% calc(100% - 9px),calc(100% - 9px) 100%,0 100%);}
.msg.me{align-self:flex-end;background:linear-gradient(150deg,rgba(168,101,232,.28),rgba(122,79,174,.16));color:var(--i0);
  box-shadow:inset 0 0 0 1px rgba(203,164,245,.35);}
.msg.you{align-self:flex-start;background:linear-gradient(150deg,rgba(29,22,48,.8),rgba(8,6,12,.9));
  box-shadow:inset 0 0 0 1px var(--line);}
.msg .t{font-family:var(--fm);font-size:9px;color:var(--i3);margin-top:4px;}

/* story viewer */
#sv{position:fixed;inset:0;z-index:820;background:#05040a;display:none;flex-direction:column;}
#sv.on{display:flex;}
#sv .bars{display:flex;gap:4px;padding:10px 12px 6px;}
#sv .bars i{flex:1;height:2.5px;background:rgba(244,239,255,.22);overflow:hidden;}
#sv .bars i b{display:block;height:100%;width:0;background:var(--vibg);}
#sv .hd{display:flex;align-items:center;gap:10px;padding:4px 14px 10px;}
#sv .hd .av{width:34px;height:34px;}
#sv .hd .n{font-family:var(--fu);font-size:14px;color:var(--i0);font-weight:600;}
#sv .hd .t{font-family:var(--fm);font-size:10px;color:var(--i3);}
#sv .im{flex:1;display:flex;align-items:center;justify-content:center;overflow:hidden;}
#sv .im img,#sv .im video{max-width:100%;max-height:100%;object-fit:contain;}
#sv .zones{position:absolute;inset:0;display:flex;}
#sv .zones div{flex:1;}

/* modale */
.veil{position:fixed;inset:0;z-index:700;background:rgba(5,4,10,.86);backdrop-filter:blur(5px);opacity:0;visibility:hidden;transition:all .35s var(--ez);}
.veil.on{opacity:1;visibility:visible;}
.modal{position:fixed;z-index:701;left:50%;top:50%;transform:translate(-50%,-46%) scale(.96);width:min(560px,94vw);max-height:88vh;
  opacity:0;visibility:hidden;transition:all .4s var(--ezo);display:flex;flex-direction:column;
  background:linear-gradient(160deg,rgba(29,22,48,.96),rgba(6,5,11,.98));backdrop-filter:blur(18px);
  box-shadow:inset 0 0 0 1px rgba(203,164,245,.34),0 40px 100px rgba(0,0,0,.85);
  clip-path:polygon(0 20px,20px 0,calc(100% - 20px) 0,100% 20px,100% calc(100% - 20px),calc(100% - 20px) 100%,20px 100%,0 calc(100% - 20px));}
.modal.on{opacity:1;visibility:visible;transform:translate(-50%,-50%) scale(1);}
.mh{display:flex;justify-content:space-between;align-items:center;padding:15px 20px;border-bottom:1px solid var(--line);gap:12px;flex:none;}
.mb{padding:18px 20px;overflow-y:auto;}
.x{width:28px;height:28px;background:transparent;border:none;box-shadow:inset 0 0 0 1px var(--line);color:var(--i2);cursor:pointer;flex:none;}
.x:hover{color:var(--redg);box-shadow:inset 0 0 0 1px var(--red);}
#toasts{position:fixed;bottom:86px;left:50%;transform:translateX(-50%);z-index:800;display:flex;flex-direction:column;gap:8px;width:min(340px,92vw);}
.toast{padding:11px 14px;font-family:var(--fu);font-size:12.5px;color:var(--i1);opacity:0;transform:translateY(12px);
  animation:ti .45s var(--ezo) forwards;background:linear-gradient(150deg,rgba(29,22,48,.96),rgba(8,6,12,.96));backdrop-filter:blur(10px);
  box-shadow:inset 0 0 0 1px rgba(168,101,232,.34);text-align:center;
  clip-path:polygon(0 9px,9px 0,100% 0,100% calc(100% - 9px),calc(100% - 9px) 100%,0 100%);}
@keyframes ti{to{opacity:1;transform:translateY(0);}}
.toast.out{animation:to .35s forwards;}@keyframes to{to{opacity:0;transform:translateY(12px);}}
.drop{padding:24px 16px;text-align:center;cursor:pointer;box-shadow:inset 0 0 0 1px var(--line);background:rgba(21,16,34,.5);transition:all .2s;
  clip-path:polygon(0 10px,10px 0,100% 0,100% calc(100% - 10px),calc(100% - 10px) 100%,0 100%);}
.drop:hover{box-shadow:inset 0 0 0 1px var(--vib);}
.drop .t{font-family:var(--fu);font-size:12.5px;color:var(--i2);letter-spacing:.05em;}
.thumbs{display:flex;gap:7px;flex-wrap:wrap;margin-top:11px;}
.thumbs .t{width:62px;height:62px;position:relative;overflow:hidden;box-shadow:inset 0 0 0 1px var(--line);}
.thumbs .t img,.thumbs .t video{width:100%;height:100%;object-fit:cover;}
.thumbs .t button{position:absolute;top:2px;right:2px;width:17px;height:17px;background:rgba(8,6,12,.8);border:none;color:var(--redg);cursor:pointer;font-size:11px;line-height:1;}
.empty{padding:34px 18px;text-align:center;font-family:var(--fm);font-size:12.5px;color:var(--i3);}
.warn{font-family:var(--fm);font-size:11px;color:var(--goldg);padding:9px 12px;margin-bottom:12px;
  box-shadow:inset 0 0 0 1px rgba(224,171,72,.4);background:rgba(224,171,72,.07);}

/* ==================== MOUVEMENT ====================
   Chaque élément entre en scène plutôt que d'apparaître : les
   animations portent des délais échelonnés en CSS pur, de sorte que
   l'interface reste correcte même si le script est interrompu. */

/* --- aurores de fond en dérive lente --- */
body::before{animation:aurora 26s ease-in-out infinite alternate;}
@keyframes aurora{
  0%{transform:translate3d(0,0,0) scale(1);}
  50%{transform:translate3d(-2%,1.5%,0) scale(1.06);}
  100%{transform:translate3d(2%,-1%,0) scale(1.03);}
}
body::after{animation:grain 18s linear infinite;}
@keyframes grain{to{background-position:32px 24px;}}

/* --- entrée des cartes, en cascade --- */
@keyframes cardIn{
  0%{opacity:0;transform:translateY(26px) scale(.975);filter:blur(7px);}
  60%{filter:blur(0);}
  100%{opacity:1;transform:none;filter:none;}
}
.card{animation:cardIn .62s var(--ezo) both;}
.card:nth-child(1){animation-delay:.02s;}
.card:nth-child(2){animation-delay:.10s;}
.card:nth-child(3){animation-delay:.18s;}
.card:nth-child(4){animation-delay:.26s;}
.card:nth-child(5){animation-delay:.34s;}
.card:nth-child(6){animation-delay:.42s;}
.card:nth-child(n+7){animation-delay:.5s;}
.card{transition:box-shadow .45s var(--ez),transform .45s var(--ez);}
.card:hover{box-shadow:inset 0 0 0 1px rgba(203,164,245,.42),0 22px 50px -30px rgba(168,101,232,.6);}

/* --- changement de vue --- */
@keyframes viewIn{
  0%{opacity:0;transform:translateY(16px) scale(.994);filter:blur(9px);}
  100%{opacity:1;transform:none;filter:none;}
}
#view.swap{animation:viewIn .5s var(--ezo);}
@keyframes viewOut{to{opacity:0;transform:translateY(-10px) scale(.995);filter:blur(6px);}}
#view.leaving{animation:viewOut .2s var(--ez) forwards;}

/* --- stories : anneau en rotation --- */
.ring{animation:ringSpin 5.5s linear infinite;}
@keyframes ringSpin{to{transform:rotate(360deg);}}
.ring>.av{animation:ringSpin 5.5s linear infinite reverse;}
.ring.seen{animation:none;}
.ring.seen>.av{animation:none;}
.st{transition:transform .3s var(--ez);}
.st:hover{transform:translateY(-4px);}
.st:active{transform:scale(.94);}
@keyframes stIn{from{opacity:0;transform:translateX(-14px) scale(.9);}to{opacity:1;transform:none;}}
.stories .st{animation:stIn .5s var(--ezo) both;}
.stories .st:nth-child(1){animation-delay:.04s;}
.stories .st:nth-child(2){animation-delay:.1s;}
.stories .st:nth-child(3){animation-delay:.16s;}
.stories .st:nth-child(4){animation-delay:.22s;}
.stories .st:nth-child(n+5){animation-delay:.28s;}

/* --- avatars --- */
.av{transition:transform .35s var(--ez),box-shadow .35s var(--ez);}
.av:hover{transform:scale(1.06);box-shadow:inset 0 0 0 1px var(--vibg),0 0 22px -6px rgba(168,101,232,.85);}
.post-h .av,.urow .av{cursor:pointer;}

/* --- média : arrivée en fondu-zoom --- */
@keyframes mediaIn{from{opacity:0;transform:scale(1.07);}to{opacity:1;transform:none;}}
.media img,.media video{animation:mediaIn .8s var(--ezo) both;}
.media{transition:box-shadow .4s var(--ez);}
.media .nav-a{opacity:0;transition:opacity .3s var(--ez),transform .3s var(--ez);}
.media:hover .nav-a{opacity:1;}
.media .nav-a:hover{transform:translateY(-50%) scale(1.14);}
.media .nav-a.l:hover{transform:translateY(-50%) scale(1.14) translateX(-2px);}
.media .dots i{transition:all .3s var(--ez);}
.media .dots i.on{transform:scale(1.35);}
/* balayage holographique sur le média */
.media::after{content:'';position:absolute;inset:0;pointer-events:none;z-index:2;
  background:linear-gradient(112deg,transparent 42%,rgba(203,164,245,.09) 50%,transparent 58%);
  transform:translateX(-110%);transition:transform 1s var(--ez);}
.card:hover .media::after{transform:translateX(110%);}

/* --- cœur : éclat au clic --- */
@keyframes heartPop{
  0%{transform:scale(1);}30%{transform:scale(1.42) rotate(-9deg);}
  55%{transform:scale(.88);}75%{transform:scale(1.12);}100%{transform:scale(1);}
}
.acts button.liked svg{animation:heartPop .55s var(--ezo);}
.acts button{position:relative;transition:transform .2s var(--ez),color .2s;}
.acts button:active{transform:scale(.88);}
.acts button::after{content:'';position:absolute;left:50%;top:44%;width:12px;height:12px;margin:-6px 0 0 -6px;
  border-radius:50%;border:2px solid var(--redg);opacity:0;pointer-events:none;}
.acts button.liked::after{animation:ripple .7s var(--ezo);}
@keyframes ripple{0%{opacity:.85;transform:scale(.6);}100%{opacity:0;transform:scale(3.6);}}

/* --- double-tap : grand cœur --- */
.dbl{position:absolute;left:50%;top:50%;width:110px;height:110px;margin:-55px 0 0 -55px;z-index:4;pointer-events:none;
  color:#fff;filter:drop-shadow(0 0 22px rgba(232,132,108,.9));animation:dblHeart .95s var(--ezo) forwards;}
@keyframes dblHeart{
  0%{opacity:0;transform:scale(.3) rotate(-14deg);}
  22%{opacity:1;transform:scale(1.18) rotate(4deg);}
  40%{transform:scale(.96) rotate(0);}
  70%{opacity:1;transform:scale(1);}
  100%{opacity:0;transform:scale(1.3) translateY(-24px);}
}

/* --- compteur de réactions : petit sursaut --- */
@keyframes bump{0%{transform:none;}40%{transform:translateY(-4px) scale(1.1);}100%{transform:none;}}
.pbody .likes.bump{animation:bump .45s var(--ezo);}

/* --- boutons : balayage et pression --- */
.btn{position:relative;overflow:hidden;transition:all .25s var(--ez);}
.btn::before{content:'';position:absolute;top:0;left:-120%;width:60%;height:100%;
  background:linear-gradient(90deg,transparent,rgba(203,164,245,.28),transparent);transition:left .6s var(--ez);}
.btn:hover:not(:disabled)::before{left:130%;}
.btn:active:not(:disabled){transform:scale(.95);}
.ib{transition:all .25s var(--ez);}
.ib:hover{transform:translateY(-2px);}
.ib:active{transform:scale(.9);}

/* --- navigation basse --- */
.nav button{position:relative;transition:color .25s var(--ez),transform .25s var(--ez);}
.nav button svg{transition:transform .35s var(--ezo);}
.nav button.on svg{transform:translateY(-3px) scale(1.12);}
.nav button:active{transform:scale(.9);}
.nav button::after{content:'';position:absolute;top:0;left:50%;width:0;height:2px;background:var(--vibg);
  transform:translateX(-50%);box-shadow:0 0 10px var(--vibg);transition:width .4s var(--ezo);}
.nav button.on::after{width:42%;}
@keyframes navPulse{0%{opacity:.5;transform:translateX(-50%) scaleX(.4);}100%{opacity:1;transform:translateX(-50%) scaleX(1);}}
.nav button.on::after{animation:navPulse .45s var(--ezo);}

/* --- barre supérieure --- */
.top{position:sticky;}
.top::after{content:'';position:absolute;left:0;right:0;bottom:-1px;height:1px;
  background:linear-gradient(90deg,transparent,rgba(203,164,245,.6),transparent);
  background-size:200% 100%;animation:barShine 6s linear infinite;}
@keyframes barShine{to{background-position:200% 0;}}
.top .lg svg{transition:transform .5s var(--ezo);}
.top .lg:hover svg{transform:rotate(60deg) scale(1.1);}

/* --- champs --- */
.inp,.txa{transition:box-shadow .3s var(--ez),background .3s var(--ez);}
.inp:focus,.txa:focus{background:linear-gradient(158deg,rgba(38,28,64,.82),rgba(10,8,16,.9));
  box-shadow:inset 0 0 0 1px var(--vib),0 0 22px -8px rgba(168,101,232,.8);}

/* --- grille du profil --- */
@keyframes cellIn{from{opacity:0;transform:scale(.86);}to{opacity:1;transform:none;}}
.gcell{animation:cellIn .5s var(--ezo) both;}
.gcell:nth-child(1){animation-delay:.02s;}.gcell:nth-child(2){animation-delay:.06s;}
.gcell:nth-child(3){animation-delay:.1s;}.gcell:nth-child(4){animation-delay:.14s;}
.gcell:nth-child(5){animation-delay:.18s;}.gcell:nth-child(6){animation-delay:.22s;}
.gcell:nth-child(n+7){animation-delay:.26s;}
.gcell::after{content:'';position:absolute;inset:0;background:linear-gradient(0deg,rgba(168,101,232,.35),transparent 60%);
  opacity:0;transition:opacity .35s var(--ez);}
.gcell:hover::after{opacity:1;}

/* --- lignes de compte --- */
.urow{transition:background .28s var(--ez),transform .28s var(--ez),box-shadow .28s var(--ez);}
.urow:hover{transform:translateX(5px);box-shadow:inset 3px 0 0 var(--vibg);}
@keyframes rowIn{from{opacity:0;transform:translateX(-12px);}to{opacity:1;transform:none;}}
.urow{animation:rowIn .42s var(--ezo) both;}
.urow:nth-child(1){animation-delay:.02s;}.urow:nth-child(2){animation-delay:.07s;}
.urow:nth-child(3){animation-delay:.12s;}.urow:nth-child(4){animation-delay:.17s;}
.urow:nth-child(n+5){animation-delay:.22s;}

/* --- compteurs du profil --- */
.stat{transition:transform .3s var(--ez);}
.stat:hover{transform:translateY(-3px);}
.stat .n{transition:color .3s,text-shadow .3s;}
.stat:hover .n{color:var(--vibg);text-shadow:0 0 18px rgba(168,101,232,.8);}
@keyframes statIn{from{opacity:0;transform:translateY(10px);}to{opacity:1;transform:none;}}
.stat{animation:statIn .5s var(--ezo) both;}
.stat:nth-child(1){animation-delay:.06s;}.stat:nth-child(2){animation-delay:.13s;}
.stat:nth-child(3){animation-delay:.2s;}.stat:nth-child(4){animation-delay:.27s;}

/* --- modale --- */
.modal .mb>*{animation:cardIn .5s var(--ezo) both;}
.modal .mb>*:nth-child(1){animation-delay:.05s;}
.modal .mb>*:nth-child(2){animation-delay:.11s;}
.modal .mb>*:nth-child(3){animation-delay:.17s;}
.veil{transition:opacity .4s var(--ez),visibility .4s,backdrop-filter .4s;}

/* --- messages --- */
@keyframes msgIn{from{opacity:0;transform:translateY(12px) scale(.94);}to{opacity:1;transform:none;}}
.msg{animation:msgIn .4s var(--ezo) both;}
.msg.me{transform-origin:right bottom;}
.msg.you{transform-origin:left bottom;}

/* --- notifications --- */
.toast{position:relative;overflow:hidden;}
.toast::after{content:'';position:absolute;left:0;bottom:0;height:2px;width:100%;
  background:linear-gradient(90deg,var(--vibg),var(--turg));transform-origin:left;animation:tprog 3.4s linear forwards;}
@keyframes tprog{to{transform:scaleX(0);}}

/* --- vignettes de brouillon --- */
@keyframes thumbIn{from{opacity:0;transform:scale(.7) rotate(-6deg);}to{opacity:1;transform:none;}}
.thumbs .t{animation:thumbIn .42s var(--ezo) both;transition:transform .25s var(--ez);}
.thumbs .t:hover{transform:scale(1.07);}

/* --- zone de dépôt --- */
.drop{transition:all .3s var(--ez);}
.drop:hover{transform:translateY(-2px);background:rgba(29,22,48,.7);}

/* --- lecteur de story --- */
@keyframes svIn{from{opacity:0;transform:scale(1.05);}to{opacity:1;transform:none;}}
#sv.on{animation:svIn .38s var(--ezo);}
#sv .im img,#sv .im video{animation:mediaIn .6s var(--ezo) both;}

/* --- amorçage --- */
@keyframes bootOut{to{opacity:0;transform:scale(1.08);filter:blur(14px);}}
#boot.gone{animation:bootOut .8s var(--ez) forwards;}
.bt{animation:cardIn .9s var(--ezo) both;animation-delay:.15s;}
.bs{animation:cardIn .9s var(--ezo) both;animation-delay:.35s;}

/* --- barre de défilement --- */
::-webkit-scrollbar{width:8px;height:8px;}
::-webkit-scrollbar-track{background:rgba(8,6,12,.5);}
::-webkit-scrollbar-thumb{background:linear-gradient(180deg,var(--vib2),var(--vib));border-radius:4px;}
::-webkit-scrollbar-thumb:hover{background:var(--vibg);}

/* --- respect des préférences système --- */
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:.01ms !important;animation-iteration-count:1 !important;
    transition-duration:.01ms !important;}
}

/* ==================== TÉLÉPHONE ====================
   Même interface, ajustée aux écrans étroits : encoches iOS,
   zones tactiles suffisantes et champs à 16 px pour éviter le
   zoom automatique de Safari à la saisie. */
.top{padding-top:calc(11px + env(safe-area-inset-top));}
.nav{padding-bottom:calc(9px + env(safe-area-inset-bottom));}
main{padding-bottom:calc(92px + env(safe-area-inset-bottom));}
#toasts{bottom:calc(86px + env(safe-area-inset-bottom));}
@media (max-width:560px){
  body{font-size:14.5px;}
  main{padding:12px 10px calc(96px + env(safe-area-inset-bottom));}
  .top{padding:10px 13px;padding-top:calc(10px + env(safe-area-inset-top));}
  .top .lg .n{font-size:15px;letter-spacing:.12em;}
  .card{margin-bottom:13px;}
  /* Champs à 16 px : en dessous, Safari zoome sur le formulaire. */
  .inp,.txa,.sel{font-size:16px;padding:11px 13px;}
  .btn{padding:11px 15px;}
  .btn.sm{padding:9px 12px;}
  .ib{width:38px;height:38px;}
  .nav button{padding:8px 4px;font-size:9px;}
  .nav button svg{width:21px;height:21px;}
  /* Profil : la ligne de compteurs reste sur une seule rangée */
  .phead{gap:13px;padding:15px 12px;}
  .phead .av{width:72px;height:72px;}
  .stats{gap:0;justify-content:space-between;flex-wrap:nowrap;}
  .stat{flex:1;min-width:0;}
  .stat .n{font-size:15px;}
  .stat .l{font-size:8.5px;letter-spacing:.06em;}
  .pbio{padding:0 12px 13px;}
  .post-h{padding:11px 12px;}
  .post-h .av{width:34px;height:34px;}
  .pbody{padding:0 12px 12px;}
  .acts{padding:9px 9px 5px;}
  .acts button{padding:7px;}
  .acts button svg{width:23px;height:23px;}
  .st{width:60px;}
  .st .av{width:54px;height:54px;}
  .stories{gap:10px;}
  .media .nav-a{width:34px;height:34px;}
  .thumbs .t{width:56px;height:56px;}
  .modal{width:96vw;max-height:90vh;}
  .mb{padding:16px;}
  .mh{padding:13px 16px;}
  .thread{max-height:46vh;}
  .msg{max-width:84%;}
  /* Les trois champs de compteurs passent en colonne */
  .mb div[style*="grid-template-columns:1fr 1fr 1fr"]{grid-template-columns:1fr !important;}
}
@media (max-width:380px){
  .stat .l{font-size:8px;}
  .top .lg .n{font-size:13.5px;}
  .grid3{gap:2px;}
}
</style>
</head>
<body>

<canvas id="dust"></canvas>

<div id="boot">
  <canvas id="bpart"></canvas>
  <div class="bstage">
    <svg class="brib" id="brib" viewBox="-160 -160 320 320"></svg>
    <svg class="bgrid" id="bgrid" viewBox="-160 -160 320 320"></svg>
    <svg class="bfil" id="bfil" viewBox="-160 -160 320 320"></svg>
    <div class="bcore"></div>
    <svg class="bglyphs" id="bglyphs" viewBox="-100 -100 200 200"></svg>
    <svg class="blogo" id="benter" viewBox="0 0 100 100" role="button" tabindex="0" aria-label="Entrer sur le réseau">
      <circle class="bhalo" cx="50" cy="50" r="46"/>
      <circle class="bhit" cx="50" cy="50" r="48" fill="transparent"/>
      <g id="bfrag"></g>
      <circle class="bhub" cx="50" cy="50" r="10"/>
      <circle class="barc" cx="50" cy="50" r="40"/>
    </svg>
    <div class="bwave"></div><div class="bwave w2"></div>
  </div>
  <div class="bt" id="bt"></div>
  <div class="bs" id="bs">Connexion au réseau…</div>
  <div class="bname" id="bname"><span class="l1">NDABA</span><span class="l2">Réseau</span></div>
  <div class="bskip" id="bskip">Toucher l’emblème pour entrer</div>
  <button class="bsnd" id="bsnd" title="Son"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M11 5 6 9H3v6h3l5 4Z"/><path d="M15.5 8.5a5 5 0 0 1 0 7"/><path d="M18.5 5.5a9 9 0 0 1 0 13"/></svg></button>
  <div class="bflash" id="bflash"></div>
  <div class="biris" id="biris"></div>
</div>

<div id="app" style="display:none;">
  <div class="top">
    <div class="lg" id="logo">
      <svg viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="6"><path d="M50 8 L84 28 L84 72 L50 92 L16 72 L16 28 Z"/><circle cx="50" cy="50" r="11" fill="currentColor" stroke="none"/></svg>
      <span class="n">NDABA</span>
    </div>
    <div class="rt">
      <button class="ib" id="b-dm" title="Messages"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M21 12a8.5 8.5 0 0 1-12.2 7.7L3 21l1.4-5.4A8.5 8.5 0 1 1 21 12Z"/></svg><span class="badge" id="dm-badge" style="display:none">0</span></button>
      <button class="ib" id="b-switch" title="Changer de compte"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M16 3h5v5M21 3l-7 7M8 21H3v-5M3 21l7-7"/></svg></button>
    </div>
  </div>

  <main id="view"></main>

  <div class="nav" id="nav">
    <button data-v="feed" class="on"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M3 10 12 3l9 7v10a1 1 0 0 1-1 1h-5v-6H9v6H4a1 1 0 0 1-1-1Z"/></svg>Fil</button>
    <button data-v="search"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><circle cx="11" cy="11" r="7"/><path d="m20 20-4.3-4.3"/></svg>Explorer</button>
    <button data-v="create"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><rect x="3" y="3" width="18" height="18" rx="3"/><path d="M12 8v8M8 12h8"/></svg>Publier</button>
    <button data-v="me"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4.4 3.6-8 8-8s8 3.6 8 8"/></svg>Profil</button>
  </div>
</div>

<div id="sv"></div>
<div class="veil" id="veil"></div>
<div class="modal" id="modal"><div class="mh"><div class="eyebrow" id="mt">—</div><button class="x" id="mx">✕</button></div><div class="mb" id="mb"></div></div>
<div id="toasts"></div>

<script>
(function(){
'use strict';

const WAK_PATHS = {
  a:"M 16.40 8.00 L 16.40 54.20 L 37.40 54.20 L 45.80 62.60 L 45.80 92.00 L 54.20 92.00 L 54.20 62.60 L 62.60 54.20 L 83.60 54.20 L 83.60 8.00 L 75.20 12.20 L 71.00 50.00 L 58.40 50.00 L 50.00 29.00 L 45.80 29.00 L 45.80 45.80 L 29.00 50.00 L 20.60 41.60 L 20.60 8.00 Z",
  b:"M 71.00 8.00 L 45.80 8.00 L 45.80 92.00 L 50.00 92.00 L 50.00 20.60 L 71.00 16.40 Z M 29.00 8.00 L 29.00 92.00 L 37.40 92.00 L 37.40 8.00 Z",
  c:"M 47.90 8.00 L 47.90 37.40 L 39.50 45.80 L 14.30 50.00 L 14.30 92.00 L 22.70 92.00 L 26.90 54.20 L 43.70 54.20 L 47.90 66.80 L 56.30 66.80 L 60.50 54.20 L 73.10 54.20 L 77.30 92.00 L 85.70 92.00 L 85.70 45.80 L 60.50 45.80 L 56.30 8.00 Z",
  d:"M 39.50 33.20 L 43.70 50.00 L 52.10 54.20 L 52.10 41.60 Z M 18.50 8.00 L 22.70 16.40 L 68.90 16.40 L 73.10 20.60 L 73.10 79.40 L 68.90 83.60 L 22.70 83.60 L 18.50 92.00 L 81.50 92.00 L 81.50 8.00 Z",
  e:"M 16.40 8.00 L 45.80 50.00 L 16.40 92.00 L 83.60 92.00 L 83.60 83.60 L 58.40 54.20 L 83.60 16.40 L 83.60 8.00 Z M 37.40 75.20 L 54.20 62.60 L 66.80 79.40 L 41.60 83.60 Z M 37.40 24.80 L 41.60 16.40 L 66.80 20.60 L 50.00 41.60 Z",
  f:"M 45.80 45.80 L 45.80 50.00 L 54.20 50.00 L 54.20 45.80 Z M 37.40 8.00 L 20.60 20.60 L 12.20 58.40 L 29.00 87.80 L 62.60 92.00 L 79.40 79.40 L 87.80 62.60 L 87.80 37.40 L 71.00 12.20 Z M 41.60 16.40 L 58.40 16.40 L 79.40 41.60 L 79.40 58.40 L 58.40 83.60 L 41.60 83.60 L 20.60 58.40 L 24.80 33.20 Z",
  g:"M 20.60 8.00 L 20.60 16.40 L 58.40 33.20 L 16.40 50.00 L 58.40 71.00 L 20.60 83.60 L 20.60 92.00 L 83.60 75.20 L 79.40 66.80 L 45.80 54.20 L 50.00 45.80 L 79.40 37.40 L 83.60 29.00 Z",
  h:"M 45.80 8.00 L 41.60 20.60 L 24.80 37.40 L 20.60 66.80 L 37.40 92.00 L 62.60 92.00 L 79.40 75.20 L 79.40 45.80 L 62.60 24.80 L 62.60 12.20 Z M 45.80 33.20 L 58.40 33.20 L 71.00 45.80 L 71.00 71.00 L 58.40 83.60 L 45.80 83.60 L 29.00 62.60 L 33.20 45.80 Z",
  i:"M 22.70 8.00 L 22.70 20.60 L 43.70 54.20 L 18.50 92.00 L 26.90 92.00 L 47.90 62.60 L 73.10 92.00 L 81.50 92.00 L 56.30 50.00 L 81.50 16.40 L 81.50 8.00 L 73.10 8.00 L 52.10 37.40 Z",
  j:"M 43.70 8.00 L 35.30 16.40 L 43.70 33.20 L 43.70 50.00 L 22.70 66.80 L 14.30 92.00 L 22.70 92.00 L 26.90 79.40 L 43.70 62.60 L 56.30 62.60 L 73.10 79.40 L 77.30 92.00 L 85.70 92.00 L 81.50 71.00 L 52.10 50.00 L 60.50 12.20 Z",
  k:"M 34.53 8.00 L 52.21 34.53 L 38.95 43.37 L 12.42 30.11 L 12.42 38.95 L 25.68 47.79 L 12.42 69.89 L 38.95 56.63 L 52.21 69.89 L 38.95 83.16 L 43.37 92.00 L 83.16 61.05 L 87.58 47.79 L 52.21 12.42 Z M 61.05 38.95 L 74.32 52.21 L 65.47 61.05 L 52.21 52.21 Z",
  l:"M 16.40 8.00 L 16.40 24.80 L 58.40 24.80 L 62.60 29.00 L 62.60 71.00 L 58.40 75.20 L 16.40 75.20 L 16.40 92.00 L 83.60 92.00 L 79.40 83.60 L 83.60 79.40 L 83.60 12.20 L 79.40 8.00 Z",
  m:"M 24.80 8.00 L 24.80 92.00 L 33.20 92.00 L 75.20 71.00 L 71.00 62.60 L 45.80 50.00 L 71.00 37.40 L 75.20 29.00 Z M 33.20 75.20 L 37.40 58.40 L 54.20 66.80 L 37.40 79.40 Z M 33.20 24.80 L 37.40 20.60 L 50.00 33.20 L 37.40 41.60 Z",
  n:"M 52.21 8.00 L 52.21 92.00 L 61.05 92.00 L 61.05 34.53 L 65.47 30.11 L 78.74 43.37 L 87.58 34.53 L 61.05 8.00 Z M 38.95 8.00 L 12.42 38.95 L 21.26 43.37 L 34.53 25.68 L 38.95 30.11 L 38.95 92.00 L 43.37 92.00 L 43.37 8.00 Z",
  o:"M 14.30 54.20 L 14.30 92.00 L 22.70 87.80 L 26.90 58.40 L 68.90 58.40 L 77.30 66.80 L 77.30 92.00 L 85.70 87.80 L 85.70 54.20 Z M 14.30 8.00 L 14.30 45.80 L 85.70 45.80 L 85.70 8.00 L 77.30 8.00 L 73.10 37.40 L 26.90 37.40 L 22.70 8.00 Z",
  p:"M 46.00 40.00 L 46.00 48.00 L 58.00 52.00 L 58.00 44.00 Z M 74.00 8.00 L 26.00 8.00 L 22.00 12.00 L 22.00 76.00 L 26.00 80.00 L 22.00 88.00 L 30.00 92.00 L 30.00 24.00 L 38.00 16.00 L 78.00 16.00 Z",
  q:"M 16.00 8.00 L 16.00 28.00 L 24.00 44.00 L 32.00 48.00 L 16.00 72.00 L 16.00 92.00 L 24.00 92.00 L 24.00 76.00 L 36.00 60.00 L 48.00 72.00 L 44.00 76.00 L 48.00 92.00 L 52.00 92.00 L 56.00 60.00 L 76.00 76.00 L 76.00 92.00 L 84.00 92.00 L 84.00 72.00 L 68.00 52.00 L 84.00 28.00 L 84.00 8.00 L 76.00 12.00 L 76.00 24.00 L 64.00 40.00 L 52.00 36.00 L 52.00 8.00 L 48.00 8.00 L 48.00 24.00 L 40.00 40.00 L 28.00 32.00 L 24.00 12.00 Z",
  r:"M 14.30 12.20 L 18.50 29.00 L 47.90 50.00 L 47.90 92.00 L 52.10 92.00 L 56.30 83.60 L 52.10 50.00 L 81.50 33.20 L 85.70 12.20 L 77.30 12.20 L 77.30 20.60 L 64.70 33.20 L 56.30 29.00 L 52.10 8.00 L 47.90 8.00 L 43.70 33.20 L 35.30 33.20 L 22.70 12.20 Z",
  s:"M 60.50 45.80 L 60.50 54.20 L 68.90 54.20 Z M 56.30 8.00 L 39.50 20.60 L 31.10 37.40 L 31.10 66.80 L 43.70 83.60 L 64.70 92.00 L 68.90 83.60 L 56.30 79.40 L 39.50 62.60 L 43.70 33.20 L 68.90 12.20 L 68.90 8.00 Z",
  t:"M 20.60 12.20 L 33.20 45.80 L 16.40 92.00 L 24.80 92.00 L 50.00 29.00 L 75.20 87.80 L 83.60 92.00 L 79.40 66.80 L 54.20 8.00 L 45.80 8.00 L 37.40 24.80 L 29.00 12.20 Z",
  u:"M 34.00 8.00 L 30.00 16.00 L 42.00 28.00 L 30.00 40.00 L 22.00 60.00 L 26.00 80.00 L 46.00 92.00 L 70.00 88.00 L 78.00 80.00 L 78.00 52.00 L 62.00 28.00 L 70.00 8.00 L 54.00 16.00 Z M 50.00 32.00 L 70.00 56.00 L 70.00 72.00 L 58.00 84.00 L 38.00 80.00 L 30.00 68.00 L 38.00 44.00 Z",
  v:"M 16.40 8.00 L 16.40 92.00 L 83.60 92.00 L 83.60 8.00 L 62.60 12.20 L 62.60 71.00 L 58.40 75.20 L 37.40 71.00 L 37.40 8.00 Z",
  w:"M 40.00 8.00 L 20.00 32.00 L 20.00 40.00 L 28.00 40.00 L 32.00 32.00 L 36.00 36.00 L 36.00 88.00 L 44.00 92.00 L 44.00 20.00 L 68.00 16.00 L 72.00 20.00 L 72.00 88.00 L 80.00 92.00 L 80.00 12.00 Z",
  x:"M 24.80 8.00 L 24.80 92.00 L 33.20 87.80 L 33.20 66.80 L 62.60 54.20 L 66.80 92.00 L 75.20 87.80 L 75.20 45.80 L 37.40 54.20 L 33.20 50.00 L 33.20 8.00 Z",
  y:"M 16.00 8.00 L 20.00 24.00 L 40.00 44.00 L 16.00 48.00 L 16.00 56.00 L 36.00 60.00 L 16.00 84.00 L 16.00 92.00 L 24.00 92.00 L 56.00 56.00 L 84.00 56.00 L 84.00 48.00 L 56.00 48.00 Z",
  z:"M 64.70 8.00 L 60.50 37.40 L 39.50 24.80 L 26.90 24.80 L 26.90 75.20 L 60.50 58.40 L 64.70 87.80 L 73.10 92.00 L 73.10 8.00 Z M 35.30 41.60 L 39.50 37.40 L 52.10 50.00 L 39.50 58.40 Z"
};

function gly(c){const d=WAK_PATHS[c.toLowerCase()];return d?'<svg viewBox="0 0 100 100"><path d="'+d+'" fill="currentColor" fill-rule="evenodd"/></svg>':'';}
function wak(p){return String(p).split(' ').map(function(w){return '<span class="gw">'+Array.from(w).map(function(c){return /[a-zA-Z]/.test(c)?gly(c):'';}).join('')+'</span>';}).join(' ');}
function esc(s){return String(s==null?'':s).replace(/[&<>"']/g,function(c){return {'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c];});}
function uid(p){return (p||'x')+Date.now().toString(36)+Math.random().toString(36).slice(2,7);}
/* Abréviation des compteurs : 1 k, 24,5 k, 1,2 M — le nombre exact
   reste consultable en infobulle. */
function fmt(n){
  n=Number(n)||0;
  if(n<1000)return String(n);
  if(n<1000000){
    const k=n/1000;
    return (k<100?trim(k):Math.round(k))+' k';
  }
  if(n<1000000000){
    const m=n/1000000;
    return (m<100?trim(m):Math.round(m))+' M';
  }
  return trim(n/1000000000)+' Md';
}
function trim(v){
  const r=Math.round(v*10)/10;
  return String(r).replace('.',',');
}
function ago(ts){
  const s=Math.floor((Date.now()-ts)/1000);
  if(s<60)return 'à l’instant';
  if(s<3600)return Math.floor(s/60)+' min';
  if(s<86400)return Math.floor(s/3600)+' h';
  if(s<604800)return Math.floor(s/86400)+' j';
  return new Date(ts).toLocaleDateString('fr-FR');
}

/* ================= STOCKAGE ================= */
/* Les comptes, publications et messages sont conservés dans le
   stockage partagé de l'artefact : toute personne ouvrant ce lien
   rejoint le même réseau. En cas d'indisponibilité, on bascule sur
   une mémoire de session pour que l'interface reste utilisable. */
const mem={};let storeOK=true;
async function sget(k,shared){
  try{
    const r=await window.storage.get(k,shared===undefined?true:shared);
    return r&&r.value?JSON.parse(r.value):null;
  }catch(e){ return (k in mem)?mem[k]:null; }
}
async function sset(k,v,shared){
  mem[k]=v;
  try{ await window.storage.set(k,JSON.stringify(v),shared===undefined?true:shared); }
  catch(e){ storeOK=false; }
}
const K={idx:'ndaba:index',user:function(i){return 'ndaba:u:'+i;},post:function(i){return 'ndaba:p:'+i;},
  story:function(i){return 'ndaba:s:'+i;},dm:function(a,b){return 'ndaba:dm:'+[a,b].sort().join('-');},ses:'ndaba:session'};

let IDX={users:[],posts:[],stories:[],follows:{},friends:{}};
let SES={accounts:[],current:null};
let ME=null;
const ucache={},pcache={};

async function loadIndex(){
  const i=await sget(K.idx,true);
  if(i&&i.users){IDX=i;IDX.follows=IDX.follows||{};IDX.friends=IDX.friends||{};}
}
async function saveIndex(){ await sset(K.idx,IDX,true); }
async function getUser(id){
  if(ucache[id])return ucache[id];
  const u=await sget(K.user(id),true);
  if(u)ucache[id]=u;
  return u;
}
async function saveUser(u){ ucache[u.id]=u; await sset(K.user(u.id),u,true); }
async function getPost(id){
  if(pcache[id])return pcache[id];
  const p=await sget(K.post(id),true);
  if(p)pcache[id]=p;
  return p;
}
async function savePost(p){ pcache[p.id]=p; await sset(K.post(p.id),p,true); }

/* ================= OUTILS UI ================= */
function toast(m){
  const w=document.getElementById('toasts'),e=document.createElement('div');
  e.className='toast';e.textContent=m;w.appendChild(e);
  setTimeout(function(){e.classList.add('out');setTimeout(function(){e.remove();},380);},3400);
}
const veil=document.getElementById('veil'),modal=document.getElementById('modal');
function openModal(t,h){document.getElementById('mt').textContent=t;document.getElementById('mb').innerHTML=h;veil.classList.add('on');modal.classList.add('on');}
function closeModal(){veil.classList.remove('on');modal.classList.remove('on');}
veil.addEventListener('click',closeModal);document.getElementById('mx').addEventListener('click',closeModal);
document.addEventListener('keydown',function(e){if(e.key==='Escape'){closeModal();closeStory();}});
function avHTML(u,cls,ring){
  const inner=u&&u.avatar?'<img src="'+u.avatar+'" alt="">':'<div class="ph">'+(u&&u.handle?esc(u.handle[0].toUpperCase()):'?')+'</div>';
  const a='<div class="av '+(cls||'')+'">'+inner+'</div>';
  return ring?'<div class="ring '+(ring==='seen'?'seen':'')+'" style="display:inline-block">'+a+'</div>':a;
}

/* ================= MÉDIA ================= */
/* Redimensionnement systématique : le stockage plafonne à 5 Mo par
   clé, une photo brute de téléphone le dépasserait à elle seule. */
function readImage(file,max,q){
  return new Promise(function(res,rej){
    const rd=new FileReader();
    rd.onerror=function(){rej(new Error('lecture'));};
    rd.onload=function(){
      const img=new Image();
      img.onload=function(){
        try{
          const sc=Math.min(1,max/Math.max(img.width,img.height));
          const c=document.createElement('canvas');
          c.width=Math.max(1,Math.round(img.width*sc));c.height=Math.max(1,Math.round(img.height*sc));
          c.getContext('2d').drawImage(img,0,0,c.width,c.height);
          res(c.toDataURL('image/jpeg',q||.72));
        }catch(e){res(rd.result);}
      };
      img.onerror=function(){res(rd.result);};
      img.src=rd.result;
    };
    rd.readAsDataURL(file);
  });
}
function readRaw(file){
  return new Promise(function(res,rej){
    const rd=new FileReader();
    rd.onerror=function(){rej(new Error('lecture'));};
    rd.onload=function(){res(rd.result);};
    rd.readAsDataURL(file);
  });
}
const VID_MAX=2600000;
async function readMedia(file){
  if(file.type.indexOf('video')===0){
    if(file.size>VID_MAX) throw new Error('Vidéo trop lourde (max 2,5 Mo). Le stockage du réseau est limité.');
    return {type:'video',src:await readRaw(file)};
  }
  return {type:'image',src:await readImage(file,1080,.72)};
}

/* ================= SESSION ================= */
async function loadSession(){
  const s=await sget(K.ses,false);
  if(s&&s.accounts)SES=s;
}
async function saveSession(){ await sset(K.ses,SES,false); }
async function setCurrent(id){
  SES.current=id;
  if(SES.accounts.indexOf(id)===-1)SES.accounts.push(id);
  await saveSession();
  ME=await getUser(id);
  go('feed');
}

/* ================= GRAPHE SOCIAL ================= */
function following(id){return IDX.follows[id]||[];}
function followers(id){
  const out=[];
  Object.keys(IDX.follows).forEach(function(k){ if(IDX.follows[k].indexOf(id)!==-1)out.push(k); });
  return out;
}
/* Compteurs affichés = valeur réelle + décalage choisi par le
   titulaire du compte. Le graphe social reste intact en dessous :
   un nouvel abonné fait toujours monter le total. */
function dispF(u){return Math.max(0,followers(u.id).length+(u.oF||0));}
function dispG(u){return Math.max(0,following(u.id).length+(u.oG||0));}
function dispA(u){return Math.max(0,friendsOf(u.id).length+(u.oA||0));}
function dispL(p){return Math.max(0,p.likes.length+(p.oL||0));}
function friendsOf(id){
  const f=following(id);
  return f.filter(function(o){return following(o).indexOf(id)!==-1;});
}
async function toggleFollow(id){
  if(!ME||id===ME.id)return;
  const l=IDX.follows[ME.id]||(IDX.follows[ME.id]=[]);
  const i=l.indexOf(id);
  if(i===-1){l.push(id);toast('Abonnement ajouté');}
  else{l.splice(i,1);toast('Abonnement retiré');}
  await saveIndex();
}

/* ================= NAVIGATION ================= */
let VIEW='feed',PROF=null,DMW=null;
function go(v,arg){
  VIEW=v;
  if(v==='profile')PROF=arg;
  if(v==='dm')DMW=arg;
  document.querySelectorAll('#nav button').forEach(function(b){
    b.classList.toggle('on',b.getAttribute('data-v')===v||(v==='me'&&b.getAttribute('data-v')==='me'));
  });
  render();
}
document.querySelectorAll('#nav button').forEach(function(b){
  b.addEventListener('click',function(){go(b.getAttribute('data-v'));});
});
document.getElementById('logo').addEventListener('click',function(){go('feed');});
document.getElementById('b-dm').addEventListener('click',function(){go('dms');});
document.getElementById('b-switch').addEventListener('click',switcher);

const V=document.getElementById('view');
function swapIn(){
  V.classList.remove('swap');
  void V.offsetWidth;
  V.classList.add('swap');
}
async function render(){
  if(!ME){await renderAuth();swapIn();return;}
  if(VIEW==='feed')await vFeed();
  else if(VIEW==='search')await vSearch();
  else if(VIEW==='create')vCreate();
  else if(VIEW==='me')await vProfile(ME.id);
  else if(VIEW==='profile')await vProfile(PROF);
  else if(VIEW==='dms')await vDms();
  else if(VIEW==='dm')await vThread(DMW);
  swapIn();
}

/* ================= AUTHENTIFICATION ================= */
async function renderAuth(){
  const known=[];
  for(const id of SES.accounts){const u=await getUser(id);if(u)known.push(u);}
  V.innerHTML='<div class="card" style="padding:24px;">'+
    '<div class="eyebrow">Réseau du Wakanda</div>'+
    '<h1 style="font-size:24px;margin:6px 0 4px;letter-spacing:.14em;">NDABA</h1>'+
    '<div style="font-size:18px;color:var(--vibg);opacity:.8;">'+wak('Ndaba')+'</div>'+
    '<p style="font-size:13.5px;color:var(--i2);margin-top:12px;">Créez votre compte pour rejoindre le réseau. Vos publications, abonnés et messages sont conservés dans le réseau lui-même : toute personne ouvrant ce lien vous y retrouvera.</p>'+
    (known.length?'<div class="lbl" style="margin-top:18px;">Comptes de cet appareil</div>'+
      known.map(function(u){return '<div class="urow" data-sw="'+u.id+'">'+avHTML(u)+'<div class="bd"><div class="h">@'+esc(u.handle)+'</div><div class="s">'+esc(u.name||'')+'</div></div></div>';}).join(''):'')+
    '<div class="lbl" style="margin-top:18px;">Nouveau compte</div>'+
    '<div style="display:flex;flex-direction:column;gap:11px;">'+
      '<div class="drop" id="a-av"><div class="t">Choisir une photo de profil</div></div>'+
      '<input type="file" id="a-file" accept="image/*" hidden>'+
      '<input class="inp" id="a-h" placeholder="Identifiant (ex. kwullem)" maxlength="20">'+
      '<input class="inp" id="a-n" placeholder="Nom affiché" maxlength="40">'+
      '<textarea class="txa" id="a-b" placeholder="Biographie" maxlength="200"></textarea>'+
      '<button class="btn" id="a-go">Créer le compte</button>'+
    '</div></div>';
  document.querySelectorAll('[data-sw]').forEach(function(r){
    r.addEventListener('click',function(){setCurrent(r.getAttribute('data-sw'));});
  });
  let av=null;
  const drop=document.getElementById('a-av'),file=document.getElementById('a-file');
  drop.addEventListener('click',function(){file.click();});
  file.addEventListener('change',async function(){
    const f=file.files&&file.files[0];if(!f)return;
    av=await readImage(f,320,.8);
    drop.innerHTML='<img src="'+av+'" style="width:74px;height:74px;object-fit:cover;border-radius:50%;margin:0 auto 8px;"><div class="t">Changer la photo</div>';
  });
  document.getElementById('a-go').addEventListener('click',async function(){
    const h=document.getElementById('a-h').value.trim().replace(/[^a-zA-Z0-9._]/g,'').toLowerCase();
    const n=document.getElementById('a-n').value.trim();
    if(h.length<3){toast('Identifiant trop court (3 caractères minimum).');return;}
    await loadIndex();
    if(IDX.users.some(function(u){return u.handle===h;})){toast('Cet identifiant est déjà pris.');return;}
    const u={id:uid('u'),handle:h,name:n||h,bio:document.getElementById('a-b').value.trim(),avatar:av,highlights:[],ts:Date.now()};
    IDX.users.push({id:u.id,handle:u.handle,name:u.name,av:av?await shrink(av,72):null});
    IDX.follows[u.id]=[];
    await saveUser(u);await saveIndex();
    SES.accounts.push(u.id);
    await setCurrent(u.id);
    toast('Bienvenue sur Ndaba, @'+h);
  });
}
function shrink(dataUrl,size){
  return new Promise(function(res){
    const img=new Image();
    img.onload=function(){
      try{
        const c=document.createElement('canvas');c.width=c.height=size;
        const s=Math.min(img.width,img.height);
        c.getContext('2d').drawImage(img,(img.width-s)/2,(img.height-s)/2,s,s,0,0,size,size);
        res(c.toDataURL('image/jpeg',.7));
      }catch(e){res(dataUrl);}
    };
    img.onerror=function(){res(dataUrl);};
    img.src=dataUrl;
  });
}
async function switcher(){
  const known=[];
  for(const id of SES.accounts){const u=await getUser(id);if(u)known.push(u);}
  openModal('Changer de compte',
    known.map(function(u){
      return '<div class="urow" data-sw2="'+u.id+'">'+avHTML(u)+'<div class="bd"><div class="h">@'+esc(u.handle)+'</div><div class="s">'+esc(u.name||'')+'</div></div>'+
        (ME&&ME.id===u.id?'<span class="eyebrow" style="color:var(--turg)">actif</span>':'')+'</div>';
    }).join('')+
    '<div style="margin-top:14px;display:flex;gap:8px;flex-wrap:wrap;">'+
    '<button class="btn sm" id="sw-new">Créer un autre compte</button>'+
    '<button class="btn sm ghost" id="sw-out">Se déconnecter</button></div>');
  document.querySelectorAll('[data-sw2]').forEach(function(r){
    r.addEventListener('click',async function(){closeModal();await setCurrent(r.getAttribute('data-sw2'));});
  });
  document.getElementById('sw-new').addEventListener('click',function(){closeModal();ME=null;render();});
  document.getElementById('sw-out').addEventListener('click',async function(){
    closeModal();SES.current=null;await saveSession();ME=null;render();
  });
}

/* ================= FIL ================= */
async function vFeed(){
  await loadIndex();
  const stories=IDX.stories.filter(function(s){return Date.now()-s.ts<86400000;});
  const byUser={};
  stories.forEach(function(s){(byUser[s.author]=byUser[s.author]||[]).push(s);});
  let sh='<div class="stories">';
  sh+='<div class="st" id="add-story">'+avHTML(ME,'','')+'<div class="h">Votre story</div></div>';
  for(const uidk of Object.keys(byUser)){
    const u=await getUser(uidk);if(!u)continue;
    sh+='<div class="st" data-sto="'+uidk+'">'+avHTML(u,'','ring')+'<div class="h">@'+esc(u.handle)+'</div></div>';
  }
  sh+='</div>';

  const ids=IDX.posts.slice(-14).reverse();
  let ph='';
  if(!ids.length){
    ph='<div class="card empty">Le réseau est encore vide. Publiez la première image du Wakanda.</div>';
  } else {
    const posts=await Promise.all(ids.map(function(p){return getPost(p.id);}));
    for(const p of posts){ if(p) ph+=await postHTML(p); }
  }
  V.innerHTML=(storeOK?'':'<div class="warn">Stockage partagé indisponible : les contenus ne seront conservés que le temps de la session.</div>')+sh+ph;
  wireStories();
  wirePosts();
}
async function postHTML(p){
  const u=await getUser(p.author);
  const liked=ME&&p.likes.indexOf(ME.id)!==-1;
  const media=p.media.map(function(m){
    return '<div class="sl">'+(m.type==='video'
      ? '<video src="'+m.src+'" controls playsinline></video>'
      : '<img src="'+m.src+'" alt="">')+'</div>';
  }).join('');
  const dots=p.media.length>1?'<div class="dots">'+p.media.map(function(_,i){return '<i class="'+(i===0?'on':'')+'"></i>';}).join('')+'</div>':'';
  const arrows=p.media.length>1?'<button class="nav-a l" data-mv="-1">‹</button><button class="nav-a r" data-mv="1">›</button><div class="cnt">1/'+p.media.length+'</div>':'';
  const cm=p.comments.slice(-2);
  let cmh='';
  for(const c of cm){
    const cu=await getUser(c.by);
    cmh+='<div class="cap"><b>@'+esc(cu?cu.handle:'?')+'</b> '+esc(c.text)+'</div>';
  }
  return '<div class="card post" data-p="'+p.id+'">'+
    '<div class="post-h">'+avHTML(u,'','')+
      '<div style="flex:1;min-width:0;"><div class="nm" data-go="'+p.author+'">@'+esc(u?u.handle:'inconnu')+'</div>'+
      '<div class="sub">'+esc(u&&u.name?u.name:'')+'</div></div></div>'+
    '<div class="media"><div class="slides">'+media+'</div>'+arrows+dots+'</div>'+
    '<div class="acts">'+
      '<button data-like="'+p.id+'" class="'+(liked?'liked':'')+'"><svg viewBox="0 0 24 24" fill="'+(liked?'currentColor':'none')+'" stroke="currentColor" stroke-width="1.7"><path d="M12 21s-8-4.9-8-10.4A4.6 4.6 0 0 1 12 7a4.6 4.6 0 0 1 8 3.6C20 16.1 12 21 12 21Z"/></svg>'+fmt(dispL(p))+'</button>'+
      '<button data-open="'+p.id+'"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M21 12a8.5 8.5 0 0 1-12.2 7.7L3 21l1.4-5.4A8.5 8.5 0 1 1 21 12Z"/></svg>'+fmt(p.comments.length)+'</button>'+
      '<span class="sp"></span>'+
      (ME&&p.author===ME.id?'<button data-ed="'+p.id+'" title="Modifier la publication"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M4 20h4L20 8l-4-4L4 16Z"/></svg></button>':'')+
      '<button data-dl="'+p.id+'" title="Télécharger en image"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.7"><path d="M12 3v12M7 11l5 5 5-5M4 21h16"/></svg></button>'+
    '</div>'+
    '<div class="pbody">'+
      '<div class="likes" title="'+dispL(p)+'">'+fmt(dispL(p))+' réaction'+(dispL(p)>1?'s':'')+'</div>'+
      (p.caption?'<div class="cap"><b>@'+esc(u?u.handle:'?')+'</b> '+esc(p.caption)+'</div>':'')+
      cmh+
      (p.comments.length>2?'<div class="cmts" data-open="'+p.id+'">Voir les '+fmt(p.comments.length)+' commentaires</div>':'<div class="cmts" data-open="'+p.id+'">Ajouter un commentaire…</div>')+
      '<div class="time">'+ago(p.ts)+'</div>'+
    '</div></div>';
}
function wirePosts(){
  V.querySelectorAll('.post').forEach(function(el){
    let idx=0;
    const slides=el.querySelector('.slides');
    const n=slides?slides.children.length:0;
    el.querySelectorAll('[data-mv]').forEach(function(b){
      b.addEventListener('click',function(e){
        e.stopPropagation();
        idx=Math.max(0,Math.min(n-1,idx+Number(b.getAttribute('data-mv'))));
        slides.style.transform='translateX('+(-idx*100)+'%)';
        el.querySelectorAll('.dots i').forEach(function(d,i){d.classList.toggle('on',i===idx);});
        const c=el.querySelector('.cnt');if(c)c.textContent=(idx+1)+'/'+n;
      });
    });
  });
  V.querySelectorAll('[data-like]').forEach(function(b){
    b.addEventListener('click',function(){applyLike(b);});
  });
  /* Double-tap sur l'image : ajoute la réaction et fait éclore un
     grand cœur, comme sur les réseaux grand public. */
  V.querySelectorAll('.post .media').forEach(function(m){
    let last=0;
    const burst=function(){
      const h=document.createElement('div');
      h.className='dbl';
      h.innerHTML='<svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 21s-8-4.9-8-10.4A4.6 4.6 0 0 1 12 7a4.6 4.6 0 0 1 8 3.6C20 16.1 12 21 12 21Z"/></svg>';
      m.appendChild(h);
      setTimeout(function(){h.remove();},960);
    };
    const tap=function(){
      const now=Date.now();
      if(now-last<380){
        const btn=m.closest('.post').querySelector('[data-like]');
        burst();
        if(btn&&!btn.classList.contains('liked'))applyLike(btn);
        last=0;
      } else last=now;
    };
    m.addEventListener('click',tap);
  });
  V.querySelectorAll('[data-open]').forEach(function(b){
    b.addEventListener('click',function(){openPost(b.getAttribute('data-open'));});
  });
  V.querySelectorAll('[data-go]').forEach(function(b){
    b.addEventListener('click',function(){go('profile',b.getAttribute('data-go'));});
  });
  V.querySelectorAll('[data-dl]').forEach(function(b){
    b.addEventListener('click',function(){downloadPost(b.getAttribute('data-dl'));});
  });
  V.querySelectorAll('[data-ed]').forEach(function(b){
    b.addEventListener('click',function(){editPost(b.getAttribute('data-ed'));});
  });
}

async function applyLike(b){
  if(!ME)return;
  const p=await getPost(b.getAttribute('data-like'));if(!p)return;
  const i=p.likes.indexOf(ME.id);
  if(i===-1)p.likes.push(ME.id);else p.likes.splice(i,1);
  await savePost(p);
  b.classList.remove('liked');
  void b.offsetWidth;
  b.classList.toggle('liked',i===-1);
  b.childNodes[1].nodeValue=fmt(dispL(p));
  b.querySelector('svg').setAttribute('fill',i===-1?'currentColor':'none');
  const lk=b.closest('.post').querySelector('.likes');
  if(lk){
    lk.textContent=fmt(dispL(p))+' réaction'+(dispL(p)>1?'s':'');
    lk.title=String(dispL(p));
    lk.classList.remove('bump');
    void lk.offsetWidth;
    lk.classList.add('bump');
  }
}

/* ================= DÉTAIL & COMMENTAIRES ================= */
async function openPost(id){
  const p=await getPost(id);if(!p)return;
  const u=await getUser(p.author);
  let cmh='';
  for(const c of p.comments){
    const cu=await getUser(c.by);
    cmh+='<div class="urow" style="padding:8px 0;cursor:default;">'+avHTML(cu,'')+
      '<div class="bd"><div class="h" style="font-size:13px;">@'+esc(cu?cu.handle:'?')+'</div>'+
      '<div style="font-size:13.5px;color:var(--i1);">'+esc(c.text)+'</div>'+
      '<div class="mono" style="font-size:9px;color:var(--i3);">'+ago(c.ts)+'</div></div></div>';
  }
  openModal('@'+(u?u.handle:'?'),
    '<div style="max-height:40vh;overflow-y:auto;">'+(cmh||'<div class="empty">Aucun commentaire.</div>')+'</div>'+
    '<div style="display:flex;gap:8px;margin-top:12px;">'+
    '<input class="inp" id="c-in" placeholder="Votre commentaire…" maxlength="220">'+
    '<button class="btn sm" id="c-go">Envoyer</button></div>');
  document.getElementById('c-go').addEventListener('click',async function(){
    const t=document.getElementById('c-in').value.trim();
    if(!t||!ME)return;
    p.comments.push({by:ME.id,text:t,ts:Date.now()});
    await savePost(p);
    closeModal();render();
    toast('Commentaire publié');
  });
}

/* ================= MODIFIER UNE PUBLICATION ================= */
async function editPost(id){
  const p=await getPost(id);
  if(!p||!ME||p.author!==ME.id)return;
  openModal('Modifier la publication',
    '<div style="display:flex;flex-direction:column;gap:11px;">'+
      '<div><label class="lbl">Légende</label><textarea class="txa" id="ep-c" maxlength="400">'+esc(p.caption||'')+'</textarea></div>'+
      '<div><label class="lbl">Réactions affichées</label><input class="inp" id="ep-l" type="number" min="0" value="'+dispL(p)+'"></div>'+
      '<p class="mono" style="font-size:10px;color:var(--i3);">Les mentions « j’aime » reçues continueront de s’ajouter à ce nombre.</p>'+
      '<div style="display:flex;gap:8px;flex-wrap:wrap;">'+
        '<button class="btn" id="ep-go">Enregistrer</button>'+
        '<button class="btn sm ghost" id="ep-del" style="color:var(--redg);">Supprimer</button></div>'+
    '</div>');
  document.getElementById('ep-go').addEventListener('click',async function(){
    p.caption=document.getElementById('ep-c').value.trim();
    const n=parseInt(document.getElementById('ep-l').value,10);
    if(!isNaN(n))p.oL=n-p.likes.length;
    await savePost(p);
    closeModal();toast('Publication mise à jour');render();
  });
  document.getElementById('ep-del').addEventListener('click',async function(){
    await loadIndex();
    IDX.posts=IDX.posts.filter(function(x){return x.id!==p.id;});
    await saveIndex();
    delete pcache[p.id];
    closeModal();toast('Publication supprimée');go('feed');
  });
}

/* ================= PUBLIER ================= */
let draft=[];
function vCreate(){
  V.innerHTML='<div class="card" style="padding:20px;">'+
    '<div class="eyebrow">Nouvelle publication</div>'+
    '<h2 style="font-size:19px;margin:6px 0 14px;">Publier sur le réseau</h2>'+
    '<div class="drop" id="c-drop"><div class="t">Ajouter des photos ou une vidéo</div></div>'+
    '<input type="file" id="c-file" accept="image/*,video/*" multiple hidden>'+
    '<div class="thumbs" id="c-th"></div>'+
    '<div style="margin-top:14px;"><label class="lbl">Légende</label><textarea class="txa" id="c-cap" placeholder="Décrivez votre publication…" maxlength="400"></textarea></div>'+
    '<div style="display:flex;gap:9px;margin-top:14px;flex-wrap:wrap;">'+
      '<button class="btn" id="c-pub" disabled>Publier</button>'+
      '<button class="btn ghost sm" id="c-sto" disabled>Publier en story</button></div>'+
    '<p class="mono" style="font-size:10.5px;color:var(--i3);margin-top:12px;">Les images sont réduites automatiquement. Vidéos acceptées jusqu’à 2,5 Mo — au-delà, le stockage du réseau ne peut les conserver.</p>'+
    '</div>';
  draft=[];
  const drop=document.getElementById('c-drop'),file=document.getElementById('c-file');
  drop.addEventListener('click',function(){file.click();});
  file.addEventListener('change',async function(){
    for(const f of Array.prototype.slice.call(file.files)){
      if(draft.length>=10){toast('10 médias maximum par publication.');break;}
      try{ draft.push(await readMedia(f)); }
      catch(e){ toast(e.message||'Fichier illisible.'); }
    }
    file.value='';
    paintThumbs();
  });
  function paintThumbs(){
    document.getElementById('c-th').innerHTML=draft.map(function(m,i){
      return '<div class="t">'+(m.type==='video'?'<video src="'+m.src+'"></video>':'<img src="'+m.src+'">')+
        '<button data-rm="'+i+'">✕</button></div>';
    }).join('');
    document.querySelectorAll('[data-rm]').forEach(function(b){
      b.addEventListener('click',function(){draft.splice(Number(b.getAttribute('data-rm')),1);paintThumbs();});
    });
    document.getElementById('c-pub').disabled=!draft.length;
    document.getElementById('c-sto').disabled=!draft.length;
  }
  document.getElementById('c-pub').addEventListener('click',async function(){
    if(!draft.length||!ME)return;
    this.disabled=true;this.textContent='Publication…';
    const p={id:uid('p'),author:ME.id,ts:Date.now(),media:draft.slice(),caption:document.getElementById('c-cap').value.trim(),likes:[],comments:[]};
    await savePost(p);
    await loadIndex();
    IDX.posts.push({id:p.id,author:p.author,ts:p.ts});
    await saveIndex();
    draft=[];toast('Publication en ligne');go('feed');
  });
  document.getElementById('c-sto').addEventListener('click',async function(){
    if(!draft.length||!ME)return;
    const s={id:uid('s'),author:ME.id,ts:Date.now(),media:draft[0]};
    await sset(K.story(s.id),s,true);
    await loadIndex();
    IDX.stories.push({id:s.id,author:ME.id,ts:s.ts});
    await saveIndex();
    draft=[];toast('Story publiée');go('feed');
  });
}

/* ================= EXPLORER ================= */
async function vSearch(){
  await loadIndex();
  V.innerHTML='<div class="card" style="padding:16px;"><input class="inp" id="q" placeholder="Rechercher un compte…"></div><div id="res"></div>';
  const paint=async function(q){
    q=(q||'').toLowerCase();
    const list=IDX.users.filter(function(u){
      return !q||u.handle.indexOf(q)!==-1||(u.name||'').toLowerCase().indexOf(q)!==-1;
    });
    if(!list.length){document.getElementById('res').innerHTML='<div class="card empty">Aucun compte trouvé.</div>';return;}
    document.getElementById('res').innerHTML='<div class="card">'+list.map(function(u){
      const isMe=ME&&u.id===ME.id;
      const f=ME&&following(ME.id).indexOf(u.id)!==-1;
      const fr=ME&&friendsOf(ME.id).indexOf(u.id)!==-1;
      return '<div class="urow">'+
        '<div class="av" style="width:44px;height:44px;" data-go="'+u.id+'">'+(u.av?'<img src="'+u.av+'">':'<div class="ph">'+esc(u.handle[0].toUpperCase())+'</div>')+'</div>'+
        '<div class="bd" data-go="'+u.id+'"><div class="h">@'+esc(u.handle)+'</div><div class="s">'+esc(u.name||'')+(fr?' · ami':'')+'</div></div>'+
        (isMe?'<span class="eyebrow" style="color:var(--turg)">vous</span>'
             :'<button class="btn sm '+(f?'ghost':'')+'" data-f="'+u.id+'">'+(f?'Abonné':'Suivre')+'</button>')+
        '</div>';
    }).join('')+'</div>';
    document.querySelectorAll('[data-f]').forEach(function(b){
      b.addEventListener('click',async function(e){
        e.stopPropagation();
        await toggleFollow(b.getAttribute('data-f'));
        paint(document.getElementById('q').value);
      });
    });
    document.querySelectorAll('#res [data-go]').forEach(function(b){
      b.addEventListener('click',function(){go('profile',b.getAttribute('data-go'));});
    });
  };
  document.getElementById('q').addEventListener('input',function(e){paint(e.target.value);});
  paint('');
}

/* ================= PROFIL ================= */
async function vProfile(id){
  await loadIndex();
  const u=await getUser(id);
  if(!u){V.innerHTML='<div class="card empty">Compte introuvable.</div>';return;}
  const mine=ME&&u.id===ME.id;
  const mypost=IDX.posts.filter(function(p){return p.author===id;}).reverse();
  const posts=await Promise.all(mypost.map(function(p){return getPost(p.id);}));
  const f=ME&&following(ME.id).indexOf(u.id)!==-1;
  const hls=(u.highlights||[]);
  V.innerHTML='<div class="card">'+
    '<div class="phead">'+avHTML(u)+
      '<div class="stats">'+
        '<div class="stat" title="'+mypost.length+'"><div class="n">'+fmt(mypost.length)+'</div><div class="l">publications</div></div>'+
        '<div class="stat" data-lst="followers" title="'+dispF(u)+'"><div class="n">'+fmt(dispF(u))+'</div><div class="l">abonnés</div></div>'+
        '<div class="stat" data-lst="following" title="'+dispG(u)+'"><div class="n">'+fmt(dispG(u))+'</div><div class="l">abonnements</div></div>'+
        '<div class="stat" data-lst="friends" title="'+dispA(u)+'"><div class="n">'+fmt(dispA(u))+'</div><div class="l">amis</div></div>'+
      '</div></div>'+
    '<div class="pbio"><div class="nm">'+esc(u.name||u.handle)+'</div>'+
      '<div class="mono" style="font-size:11px;color:var(--i3);">@'+esc(u.handle)+'</div>'+
      (u.bio?'<div class="bio">'+esc(u.bio)+'</div>':'')+
      '<div style="display:flex;gap:8px;margin-top:12px;flex-wrap:wrap;">'+
      (mine?'<button class="btn sm" id="p-edit">Modifier le profil</button><button class="btn sm ghost" id="p-hl">Story à la une</button>'
           :'<button class="btn sm '+(f?'ghost':'')+'" id="p-f">'+(f?'Abonné':'Suivre')+'</button><button class="btn sm ghost" id="p-dm">Message</button>')+
      '</div></div>'+
    (hls.length?'<div class="hls">'+hls.map(function(h,i){
      return '<div class="hl" data-hl="'+i+'"><div class="ring seen"><div class="av" style="width:56px;height:56px;">'+
        (h.cover?'<img src="'+h.cover+'">':'<div class="ph">★</div>')+'</div></div><div class="t">'+esc(h.title)+'</div></div>';
    }).join('')+'</div>':'')+
    '</div>'+
    (posts.length?'<div class="grid3">'+posts.map(function(p){
      if(!p)return '';
      const m=p.media[0];
      return '<div class="gcell" data-op="'+p.id+'">'+(m.type==='video'?'<video src="'+m.src+'"></video>':'<img src="'+m.src+'">')+
        (p.media.length>1?'<div class="multi"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="8" y="3" width="13" height="13" rx="2"/><path d="M3 8v11a2 2 0 0 0 2 2h11"/></svg></div>':'')+'</div>';
    }).join('')+'</div>':'<div class="card empty">Aucune publication.</div>');

  V.querySelectorAll('[data-op]').forEach(function(c){
    c.addEventListener('click',function(){openPost(c.getAttribute('data-op'));});
  });
  V.querySelectorAll('[data-lst]').forEach(function(s){
    s.addEventListener('click',function(){showList(id,s.getAttribute('data-lst'));});
  });
  const pf=document.getElementById('p-f');
  if(pf)pf.addEventListener('click',async function(){await toggleFollow(id);vProfile(id);});
  const pd=document.getElementById('p-dm');
  if(pd)pd.addEventListener('click',function(){go('dm',id);});
  const pe=document.getElementById('p-edit');
  if(pe)pe.addEventListener('click',function(){editProfile();});
  const ph=document.getElementById('p-hl');
  if(ph)ph.addEventListener('click',function(){addHighlight();});
  V.querySelectorAll('[data-hl]').forEach(function(h){
    h.addEventListener('click',function(){
      const item=(u.highlights||[])[Number(h.getAttribute('data-hl'))];
      if(item&&item.storyIds&&item.storyIds.length)playStories(item.storyIds,u);
      else toast('Cette story à la une est vide.');
    });
  });
}
async function showList(id,kind){
  const ids=kind==='followers'?followers(id):(kind==='following'?following(id):friendsOf(id));
  const title={followers:'Abonnés',following:'Abonnements',friends:'Amis'}[kind];
  let h='';
  for(const i of ids){
    const u=await getUser(i);
    if(u)h+='<div class="urow" data-g2="'+u.id+'">'+avHTML(u)+'<div class="bd"><div class="h">@'+esc(u.handle)+'</div><div class="s">'+esc(u.name||'')+'</div></div></div>';
  }
  openModal(title,h||'<div class="empty">Personne pour l’instant.</div>');
  document.querySelectorAll('[data-g2]').forEach(function(r){
    r.addEventListener('click',function(){closeModal();go('profile',r.getAttribute('data-g2'));});
  });
}
function editProfile(){
  openModal('Modifier le profil',
    '<div style="display:flex;flex-direction:column;gap:11px;">'+
    '<div class="drop" id="e-av">'+(ME.avatar?'<img src="'+ME.avatar+'" style="width:74px;height:74px;object-fit:cover;border-radius:50%;margin:0 auto 8px;">':'')+'<div class="t">Changer la photo de profil</div></div>'+
    '<input type="file" id="e-file" accept="image/*" hidden>'+
    '<div><label class="lbl">Nom affiché</label><input class="inp" id="e-n" value="'+esc(ME.name||'')+'" maxlength="40"></div>'+
    '<div><label class="lbl">Biographie</label><textarea class="txa" id="e-b" maxlength="200">'+esc(ME.bio||'')+'</textarea></div>'+
    '<div class="lbl" style="margin-top:4px;">Compteurs affichés</div>'+
    '<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px;">'+
      '<div><label class="lbl">Abonnés</label><input class="inp" id="e-f" type="number" min="0" value="'+dispF(ME)+'"></div>'+
      '<div><label class="lbl">Abonnements</label><input class="inp" id="e-g" type="number" min="0" value="'+dispG(ME)+'"></div>'+
      '<div><label class="lbl">Amis</label><input class="inp" id="e-a" type="number" min="0" value="'+dispA(ME)+'"></div>'+
    '</div>'+
    '<p class="mono" style="font-size:10px;color:var(--i3);">Ces nombres sont ceux affichés sur votre profil. Les abonnements réels continuent de s’ajouter par-dessus.</p>'+
    '<button class="btn" id="e-go">Enregistrer</button></div>');
  let av=ME.avatar;
  const d=document.getElementById('e-av'),f=document.getElementById('e-file');
  d.addEventListener('click',function(){f.click();});
  f.addEventListener('change',async function(){
    const x=f.files&&f.files[0];if(!x)return;
    av=await readImage(x,320,.8);
    d.innerHTML='<img src="'+av+'" style="width:74px;height:74px;object-fit:cover;border-radius:50%;margin:0 auto 8px;"><div class="t">Changer la photo</div>';
  });
  document.getElementById('e-go').addEventListener('click',async function(){
    ME.name=document.getElementById('e-n').value.trim()||ME.handle;
    ME.bio=document.getElementById('e-b').value.trim();
    ME.avatar=av;
    /* On enregistre l'écart au réel, pour que le compteur suive
       ensuite les vrais abonnements. */
    const nf=parseInt(document.getElementById('e-f').value,10);
    const ng=parseInt(document.getElementById('e-g').value,10);
    const na=parseInt(document.getElementById('e-a').value,10);
    if(!isNaN(nf))ME.oF=nf-followers(ME.id).length;
    if(!isNaN(ng))ME.oG=ng-following(ME.id).length;
    if(!isNaN(na))ME.oA=na-friendsOf(ME.id).length;
    await saveUser(ME);
    await loadIndex();
    const e=IDX.users.filter(function(x){return x.id===ME.id;})[0];
    if(e){e.name=ME.name;e.av=av?await shrink(av,72):null;}
    await saveIndex();
    closeModal();toast('Profil mis à jour');go('me');
  });
}
async function addHighlight(){
  await loadIndex();
  const mine=IDX.stories.filter(function(s){return s.author===ME.id;});
  if(!mine.length){toast('Publiez d’abord une story.');return;}
  openModal('Story à la une',
    '<label class="lbl">Titre</label><input class="inp" id="h-t" placeholder="Ex. Birnin Zana" maxlength="18">'+
    '<div class="lbl" style="margin-top:12px;">Stories à inclure</div>'+
    '<div class="thumbs" id="h-l"></div>'+
    '<button class="btn" id="h-go" style="margin-top:14px;">Créer</button>');
  const sel={};
  const box=document.getElementById('h-l');
  for(const s of mine){
    const full=await sget(K.story(s.id),true);
    if(!full)continue;
    const el=document.createElement('div');
    el.className='t';el.style.cursor='pointer';
    el.innerHTML=full.media.type==='video'?'<video src="'+full.media.src+'"></video>':'<img src="'+full.media.src+'">';
    el.addEventListener('click',function(){
      if(sel[s.id]){delete sel[s.id];el.style.boxShadow='inset 0 0 0 1px var(--line)';}
      else{sel[s.id]=full;el.style.boxShadow='inset 0 0 0 2px var(--vibg)';}
    });
    box.appendChild(el);
  }
  document.getElementById('h-go').addEventListener('click',async function(){
    const t=document.getElementById('h-t').value.trim()||'À la une';
    const ids=Object.keys(sel);
    if(!ids.length){toast('Sélectionnez au moins une story.');return;}
    ME.highlights=ME.highlights||[];
    ME.highlights.push({title:t,storyIds:ids,cover:sel[ids[0]].media.src});
    await saveUser(ME);
    closeModal();toast('Story à la une créée');go('me');
  });
}

/* ================= STORIES ================= */
function wireStories(){
  const add=document.getElementById('add-story');
  if(add)add.addEventListener('click',function(){go('create');toast('Choisissez un média puis « Publier en story ».');});
  V.querySelectorAll('[data-sto]').forEach(function(s){
    s.addEventListener('click',async function(){
      const a=s.getAttribute('data-sto');
      const u=await getUser(a);
      const ids=IDX.stories.filter(function(x){return x.author===a&&Date.now()-x.ts<86400000;}).map(function(x){return x.id;});
      if(ids.length)playStories(ids,u);
    });
  });
}
let stoTimer=null;
async function playStories(ids,u){
  const sv=document.getElementById('sv');
  let i=0;
  const items=[];
  for(const id of ids){const s=await sget(K.story(id),true);if(s)items.push(s);}
  if(!items.length)return;
  sv.classList.add('on');
  function draw(){
    const s=items[i];
    sv.innerHTML='<div class="bars">'+items.map(function(_,k){return '<i><b style="width:'+(k<i?100:0)+'%"></b></i>';}).join('')+'</div>'+
      '<div class="hd">'+avHTML(u,'')+'<div style="flex:1"><div class="n">@'+esc(u.handle)+'</div><div class="t">'+ago(s.ts)+'</div></div>'+
      '<button class="x" id="sv-x">✕</button></div>'+
      '<div class="im">'+(s.media.type==='video'?'<video src="'+s.media.src+'" autoplay playsinline controls></video>':'<img src="'+s.media.src+'">')+'</div>'+
      '<div class="zones"><div id="sv-p"></div><div id="sv-n"></div></div>';
    document.getElementById('sv-x').addEventListener('click',closeStory);
    document.getElementById('sv-p').addEventListener('click',function(){if(i>0){i--;draw();}});
    document.getElementById('sv-n').addEventListener('click',next);
    const bar=sv.querySelectorAll('.bars i b')[i];
    if(bar){bar.style.transition='width 5s linear';setTimeout(function(){bar.style.width='100%';},40);}
    if(stoTimer)clearTimeout(stoTimer);
    stoTimer=setTimeout(next,5200);
  }
  function next(){ if(i<items.length-1){i++;draw();} else closeStory(); }
  draw();
}
function closeStory(){
  if(stoTimer)clearTimeout(stoTimer);
  const sv=document.getElementById('sv');
  sv.classList.remove('on');sv.innerHTML='';
}

/* ================= MESSAGES ================= */
async function vDms(){
  await loadIndex();
  const others=IDX.users.filter(function(u){return !ME||u.id!==ME.id;});
  if(!others.length){V.innerHTML='<div class="card empty">Aucun autre compte sur le réseau.</div>';return;}
  let h='<div class="card">';
  for(const u of others){
    const th=await sget(K.dm(ME.id,u.id),true);
    const last=th&&th.msgs&&th.msgs.length?th.msgs[th.msgs.length-1]:null;
    h+='<div class="urow" data-dm="'+u.id+'">'+
      '<div class="av" style="width:44px;height:44px;">'+(u.av?'<img src="'+u.av+'">':'<div class="ph">'+esc(u.handle[0].toUpperCase())+'</div>')+'</div>'+
      '<div class="bd"><div class="h">@'+esc(u.handle)+'</div><div class="s">'+(last?esc(last.text):'Démarrer la conversation')+'</div></div>'+
      (last?'<span class="mono" style="font-size:9.5px;color:var(--i3)">'+ago(last.ts)+'</span>':'')+'</div>';
  }
  V.innerHTML=h+'</div>';
  V.querySelectorAll('[data-dm]').forEach(function(r){
    r.addEventListener('click',function(){go('dm',r.getAttribute('data-dm'));});
  });
}
async function vThread(id){
  const u=await getUser(id);
  const key=K.dm(ME.id,id);
  const th=(await sget(key,true))||{msgs:[]};
  V.innerHTML='<div class="card">'+
    '<div class="post-h">'+avHTML(u,'')+'<div style="flex:1"><div class="nm" data-go="'+id+'">@'+esc(u?u.handle:'?')+'</div></div>'+
    '<button class="btn sm ghost" id="dm-back">Retour</button></div>'+
    '<div class="thread" id="th">'+(th.msgs.length?th.msgs.map(function(m){
      return '<div class="msg '+(m.from===ME.id?'me':'you')+'">'+esc(m.text)+'<div class="t">'+ago(m.ts)+'</div></div>';
    }).join(''):'<div class="empty">Aucun message.</div>')+'</div>'+
    '<div style="display:flex;gap:8px;padding:12px 14px;">'+
    '<input class="inp" id="dm-in" placeholder="Votre message…" maxlength="400">'+
    '<button class="btn sm" id="dm-go">Envoyer</button></div></div>';
  document.getElementById('dm-back').addEventListener('click',function(){go('dms');});
  V.querySelectorAll('[data-go]').forEach(function(b){b.addEventListener('click',function(){go('profile',id);});});
  const send=async function(){
    const t=document.getElementById('dm-in').value.trim();
    if(!t)return;
    th.msgs.push({from:ME.id,text:t,ts:Date.now()});
    await sset(key,th,true);
    vThread(id);
  };
  document.getElementById('dm-go').addEventListener('click',send);
  document.getElementById('dm-in').addEventListener('keydown',function(e){if(e.key==='Enter')send();});
  const box=document.getElementById('th');if(box)box.scrollTop=box.scrollHeight;
}

/* ================= TÉLÉCHARGEMENT PNG ================= */
/* La publication est redessinée sur un canevas à l'identique :
   en-tête, média, réactions, légende et commentaires. */
async function downloadPost(id){
  const p=await getPost(id);if(!p)return;
  const u=await getUser(p.author);
  const W=1080,PAD=44;
  const c=document.createElement('canvas');
  const ctx=c.getContext('2d');
  const img=await loadImg(p.media[0].type==='video'?null:p.media[0].src);
  const mediaH=W;
  let capLines=[];
  c.width=W;c.height=10;
  ctx.font='30px sans-serif';
  const capText=(p.caption?'@'+u.handle+'  '+p.caption:'');
  capLines=wrapText(ctx,capText,W-PAD*2);
  const cmts=[];
  for(const cm of p.comments.slice(-3)){
    const cu=await getUser(cm.by);
    cmts.push('@'+(cu?cu.handle:'?')+'  '+cm.text);
  }
  const H=140+mediaH+90+52+capLines.length*40+cmts.length*38+70;
  c.width=W;c.height=H;
  const g=ctx.createLinearGradient(0,0,W,H);
  g.addColorStop(0,'#1a1430');g.addColorStop(1,'#08060c');
  ctx.fillStyle=g;ctx.fillRect(0,0,W,H);
  ctx.strokeStyle='rgba(168,101,232,.45)';ctx.lineWidth=3;ctx.strokeRect(1.5,1.5,W-3,H-3);
  /* en-tête */
  if(u&&u.avatar){
    const a=await loadImg(u.avatar);
    if(a){ctx.save();ctx.beginPath();ctx.arc(PAD+40,74,40,0,6.28);ctx.clip();ctx.drawImage(a,PAD,34,80,80);ctx.restore();}
  }else{
    ctx.fillStyle='#2b2140';ctx.beginPath();ctx.arc(PAD+40,74,40,0,6.28);ctx.fill();
  }
  ctx.strokeStyle='rgba(203,164,245,.6)';ctx.lineWidth=2;ctx.beginPath();ctx.arc(PAD+40,74,41,0,6.28);ctx.stroke();
  ctx.fillStyle='#f4efff';ctx.font='600 34px sans-serif';ctx.fillText('@'+(u?u.handle:'?'),PAD+100,68);
  ctx.fillStyle='#9c8fba';ctx.font='24px sans-serif';
  ctx.fillText(fmt(u?dispF(u):0)+' abonnés · '+(u&&u.name?u.name:''),PAD+100,104);
  /* média */
  const my=140;
  ctx.fillStyle='#05040a';ctx.fillRect(0,my,W,mediaH);
  if(img){
    const s=Math.max(W/img.width,mediaH/img.height);
    const iw=img.width*s,ih=img.height*s;
    ctx.save();ctx.beginPath();ctx.rect(0,my,W,mediaH);ctx.clip();
    ctx.drawImage(img,(W-iw)/2,my+(mediaH-ih)/2,iw,ih);ctx.restore();
  }else{
    ctx.fillStyle='#6b6088';ctx.font='28px sans-serif';ctx.textAlign='center';
    ctx.fillText('vidéo',W/2,my+mediaH/2);ctx.textAlign='left';
  }
  if(p.media.length>1){
    ctx.fillStyle='rgba(8,6,12,.7)';ctx.fillRect(W-150,my+24,110,44);
    ctx.fillStyle='#f4efff';ctx.font='26px sans-serif';ctx.fillText('1/'+p.media.length,W-130,my+54);
  }
  /* actions */
  let y=my+mediaH+58;
  ctx.strokeStyle='#e8846c';ctx.lineWidth=4;
  heart(ctx,PAD+18,y-8,17);
  ctx.fillStyle='#cfc4e4';ctx.font='28px sans-serif';ctx.fillText(String(p.likes.length),PAD+56,y+2);
  ctx.strokeStyle='#9c8fba';bubble(ctx,PAD+130,y-10,18);
  ctx.fillText(fmt(p.comments.length),PAD+172,y+2);
  ctx.fillStyle='#cba4f5';ctx.font='600 20px sans-serif';ctx.textAlign='right';
  ctx.fillText('NDABA',W-PAD,y+2);ctx.textAlign='left';
  /* corps */
  y+=52;
  ctx.fillStyle='#f4efff';ctx.font='600 30px sans-serif';
  ctx.fillText(fmt(dispL(p))+' réaction'+(dispL(p)>1?'s':''),PAD,y);
  y+=44;
  ctx.font='30px sans-serif';ctx.fillStyle='#cfc4e4';
  capLines.forEach(function(l){ctx.fillText(l,PAD,y);y+=40;});
  ctx.font='26px sans-serif';ctx.fillStyle='#9c8fba';
  cmts.forEach(function(l){ctx.fillText(l.length>62?l.slice(0,62)+'…':l,PAD,y);y+=38;});
  ctx.fillStyle='#6b6088';ctx.font='22px sans-serif';
  ctx.fillText(ago(p.ts).toUpperCase(),PAD,H-32);

  const name='ndaba-'+(u?u.handle:'post')+'-'+p.id.slice(-5)+'.png';
  try{
    c.toBlob(function(b){
      if(!b){fallback();return;}
      const a=document.createElement('a');a.href=URL.createObjectURL(b);a.download=name;
      document.body.appendChild(a);a.click();
      setTimeout(function(){a.remove();URL.revokeObjectURL(a.href);},1800);
      toast('Publication enregistrée');
    },'image/png');
  }catch(e){fallback();}
  function fallback(){
    try{
      const a=document.createElement('a');a.href=c.toDataURL('image/png');a.download=name;
      document.body.appendChild(a);a.click();setTimeout(function(){a.remove();},1500);
      toast('Publication enregistrée');
    }catch(e2){toast('Téléchargement impossible dans ce navigateur.');}
  }
}
function heart(x,cx,cy,r){x.beginPath();x.moveTo(cx,cy+r*.9);x.bezierCurveTo(cx-r*1.6,cy-r*.4,cx-r*.5,cy-r*1.5,cx,cy-r*.4);x.bezierCurveTo(cx+r*.5,cy-r*1.5,cx+r*1.6,cy-r*.4,cx,cy+r*.9);x.stroke();}
function bubble(x,cx,cy,r){x.beginPath();x.arc(cx,cy,r,0,6.28);x.stroke();}
function loadImg(src){
  return new Promise(function(res){
    if(!src){res(null);return;}
    const i=new Image();i.onload=function(){res(i);};i.onerror=function(){res(null);};i.src=src;
  });
}
function wrapText(ctx,t,max){
  if(!t)return [];
  const words=t.split(' ');const lines=[];let cur='';
  words.forEach(function(w){
    const test=cur?cur+' '+w:w;
    if(ctx.measureText(test).width>max&&cur){lines.push(cur);cur=w;}else cur=test;
  });
  if(cur)lines.push(cur);
  return lines.slice(0,4);
}

/* ================= SONORITÉ D'ALLUMAGE =================
   Entièrement synthétisée dans le navigateur : aucun fichier audio,
   aucune musique existante. Gamme pentatonique et timbre de kalimba
   pour la couleur, tambour grave et hochet pour l'assise. */
let actx=null,sndOn=true,sndDone=false;
function audio(){
  if(actx)return actx;
  try{ actx=new (window.AudioContext||window.webkitAudioContext)(); }catch(e){ actx=null; }
  return actx;
}
function tone(t,freq,dur,type,vol,detune){
  const c=audio();if(!c)return;
  const o=c.createOscillator(),g=c.createGain();
  o.type=type||'sine';o.frequency.value=freq;
  if(detune)o.detune.value=detune;
  g.gain.setValueAtTime(0.0001,t);
  g.gain.exponentialRampToValueAtTime(vol,t+0.012);
  g.gain.exponentialRampToValueAtTime(0.0001,t+dur);
  o.connect(g);g.connect(c.destination);
  o.start(t);o.stop(t+dur+0.05);
}
/* Kalimba : fondamentale + harmonique brève, extinction rapide. */
function kalimba(t,freq,vol){
  tone(t,freq,1.5,'triangle',vol||0.13);
  tone(t,freq*2.02,0.5,'sine',(vol||0.13)*0.32);
  tone(t,freq*3.01,0.22,'sine',(vol||0.13)*0.12);
}
function shaker(t,vol){
  const c=audio();if(!c)return;
  const n=Math.floor(c.sampleRate*0.09);
  const b=c.createBuffer(1,n,c.sampleRate);
  const d=b.getChannelData(0);
  for(let i=0;i<n;i++)d[i]=(Math.random()*2-1)*Math.pow(1-i/n,2.4);
  const src=c.createBufferSource();src.buffer=b;
  const f=c.createBiquadFilter();f.type='highpass';f.frequency.value=3200;
  const g=c.createGain();g.gain.value=vol||0.06;
  src.connect(f);f.connect(g);g.connect(c.destination);
  src.start(t);
}
/* Tambour grave : chute de hauteur, comme une peau frappée. */
function drum(t,vol){
  const c=audio();if(!c)return;
  const o=c.createOscillator(),g=c.createGain();
  o.type='sine';
  o.frequency.setValueAtTime(110,t);
  o.frequency.exponentialRampToValueAtTime(42,t+0.42);
  g.gain.setValueAtTime(0.0001,t);
  g.gain.exponentialRampToValueAtTime(vol||0.34,t+0.014);
  g.gain.exponentialRampToValueAtTime(0.0001,t+0.75);
  o.connect(g);g.connect(c.destination);
  o.start(t);o.stop(t+0.8);
}
/* Souffle montant qui accompagne la floraison de la trame. */
function sweep(t,dur){
  const c=audio();if(!c)return;
  const n=Math.floor(c.sampleRate*dur);
  const b=c.createBuffer(1,n,c.sampleRate);
  const d=b.getChannelData(0);
  for(let i=0;i<n;i++)d[i]=(Math.random()*2-1)*0.5;
  const src=c.createBufferSource();src.buffer=b;
  const f=c.createBiquadFilter();f.type='bandpass';f.Q.value=1.4;
  f.frequency.setValueAtTime(320,t);
  f.frequency.exponentialRampToValueAtTime(5200,t+dur*0.82);
  const g=c.createGain();
  g.gain.setValueAtTime(0.0001,t);
  g.gain.linearRampToValueAtTime(0.075,t+dur*0.5);
  g.gain.exponentialRampToValueAtTime(0.0001,t+dur);
  src.connect(f);f.connect(g);g.connect(c.destination);
  src.start(t);src.stop(t+dur+0.05);
}
/* Nappe finale : accord ouvert qui reste suspendu. */
function pad(t){
  const c=audio();if(!c)return;
  [130.81,196.00,261.63,392.00].forEach(function(f,i){
    const o=c.createOscillator(),g=c.createGain();
    o.type=i%2?'sine':'triangle';o.frequency.value=f;o.detune.value=(i-1.5)*5;
    g.gain.setValueAtTime(0.0001,t);
    g.gain.linearRampToValueAtTime(0.055,t+0.7);
    g.gain.exponentialRampToValueAtTime(0.0001,t+3.2);
    o.connect(g);g.connect(c.destination);
    o.start(t);o.stop(t+3.3);
  });
}
/* Gamme pentatonique majeure — l'ossature mélodique. */
const PENTA=[523.25,587.33,698.46,783.99,1046.50];
function playIgnition(offset){
  const c=audio();if(!c||!sndOn||sndDone)return;
  sndDone=true;
  const t0=c.currentTime+0.05;
  const o=offset||0;
  const at=function(x){return t0+Math.max(0,x-o);};
  if(o<0.15)drum(at(0.10),0.36);                       // amorçage du noyau
  if(o<1.9)sweep(at(0.28),1.7);                        // floraison de la trame
  [0.5,0.72,0.94,1.16].forEach(function(x,i){
    if(o<x+0.05)shaker(at(x),0.05+i*0.008);            // texture des filaments
  });
  PENTA.forEach(function(f,i){                          // convergence de l'emblème
    const x=1.05+i*0.16;
    if(o<x+0.05)kalimba(at(x),f,0.125);
  });
  if(o<2.15)drum(at(2.05),0.3);                        // verrouillage du noyau
  if(o<2.3){kalimba(at(2.22),PENTA[4],0.16);kalimba(at(2.22),PENTA[2],0.11);}
  if(o<2.6)pad(at(2.5));                               // nappe d'ouverture
  if(o<3.0)kalimba(at(2.95),PENTA[3],0.08);            // la porte s'offre
}
/* Joué au moment où l'on franchit l'emblème, pas avant. */
function entryChime(){
  const c=audio();if(!c||!sndOn)return;
  try{ if(c.state==='suspended')c.resume(); }catch(e){}
  const t=c.currentTime+0.02;
  drum(t,0.3);
  sweep(t+0.04,0.85);
  kalimba(t+0.06,PENTA[0]*2,0.15);
  kalimba(t+0.15,PENTA[2]*2,0.11);
  kalimba(t+0.26,PENTA[4]*2,0.08);
}
function armSound(){
  const btn=document.getElementById('bsnd');
  const c=audio();
  if(!c){ if(btn)btn.style.display='none'; return; }
  /* L'état doit être relevé AVANT toute tentative de reprise :
     appeler resume() peut le faire basculer, et l'on perdrait
     l'information qu'un geste de l'utilisateur reste nécessaire. */
  const blocked=(c.state==='suspended');
  const fire=function(){
    if(btn)btn.classList.remove('pending');
    playIgnition((Date.now()-bootT0)/1000);
  };
  const tryPlay=function(){
    if(c.state==='suspended'){
      const p=c.resume();
      if(p&&p.then)p.then(fire).catch(function(){});
      else fire();
    } else fire();
  };
  if(blocked&&btn)btn.classList.add('pending');
  tryPlay();
  if(blocked){
    /* Filet de sécurité : si la reprise automatique est refusée, le
       premier contact relance la séquence, calée sur le temps écoulé. */
    const once=function(){
      document.removeEventListener('pointerdown',once,true);
      document.removeEventListener('keydown',once,true);
      if(!sndDone)tryPlay();
      if(btn)btn.classList.remove('pending');
    };
    document.addEventListener('pointerdown',once,true);
    document.addEventListener('keydown',once,true);
  }
}

/* ================= SÉQUENCE D'OUVERTURE ================= */
/* Trame hexagonale, filaments, glyphes en orbite et emblème
   reconstitué : tout est généré ici pour pouvoir échelonner
   précisément chaque retard d'animation. */
function buildIntro(){
  const R=26, rings=3;
  let hex='',fil='';
  const pts=[];
  for(let q=-rings;q<=rings;q++){
    for(let r=Math.max(-rings,-q-rings);r<=Math.min(rings,-q+rings);r++){
      const x=R*1.5*q, y=R*Math.sqrt(3)*(r+q/2);
      const ring=Math.max(Math.abs(q),Math.abs(r),Math.abs(q+r));
      pts.push({x:x,y:y,ring:ring});
      let p='';
      for(let i=0;i<6;i++){
        const a=Math.PI/180*(60*i);
        p+=(x+R*0.86*Math.cos(a)).toFixed(1)+','+(y+R*0.86*Math.sin(a)).toFixed(1)+' ';
      }
      hex+='<polygon points="'+p.trim()+'" style="animation-delay:'+(0.28+ring*0.16+Math.random()*0.1).toFixed(2)+'s"/>';
    }
  }
  document.getElementById('bgrid').innerHTML=hex;
  /* filaments : du centre vers les sommets des anneaux extérieurs */
  pts.filter(function(p){return p.ring===rings;}).forEach(function(p,i){
    fil+='<line x1="0" y1="0" x2="'+p.x.toFixed(1)+'" y2="'+p.y.toFixed(1)+
      '" style="animation-delay:'+(0.75+i*0.045).toFixed(2)+'s"/>';
  });
  document.getElementById('bfil').innerHTML=fil;
  /* glyphes wakandais en orbite */
  const letters='ndabawakanda'.split('');
  let g='';
  letters.forEach(function(c,i){
    const a=(Math.PI*2*i/letters.length)-Math.PI/2, rad=82;
    const d=WAK_PATHS[c];
    if(!d)return;
    const x=Math.cos(a)*rad, y=Math.sin(a)*rad;
    g+='<g transform="translate('+x.toFixed(1)+','+y.toFixed(1)+') scale(.12) translate(-50,-50)" '+
       'style="animation-delay:'+(1.25+i*0.06).toFixed(2)+'s"><path d="'+d+'" fill-rule="evenodd"/></g>';
  });
  document.getElementById('bglyphs').innerHTML=g;
  /* emblème : six éclats qui convergent */
  let fr='';
  for(let i=0;i<6;i++){
    const a1=Math.PI/180*(60*i-90), a2=Math.PI/180*(60*(i+1)-90);
    const x1=50+42*Math.cos(a1), y1=50+42*Math.sin(a1);
    const x2=50+42*Math.cos(a2), y2=50+42*Math.sin(a2);
    const dx=Math.cos((a1+a2)/2)*70, dy=Math.sin((a1+a2)/2)*70;
    fr+='<polygon class="frag" points="50,50 '+x1.toFixed(1)+','+y1.toFixed(1)+' '+x2.toFixed(1)+','+y2.toFixed(1)+'" '+
        'style="--fx:'+dx.toFixed(0)+'px;--fy:'+dy.toFixed(0)+'px;--fr:'+(i%2?55:-55)+'deg;animation-delay:'+(0.95+i*0.09).toFixed(2)+'s"/>';
  }
  document.getElementById('bfrag').innerHTML=fr;
  /* rubans d'énergie : arcs qui s'enroulent autour de la scène */
  const cols=['rgba(203,164,245,.85)','rgba(104,224,214,.75)','rgba(246,209,138,.6)'];
  let rib='';
  for(let i=0;i<3;i++){
    const r1=96+i*22,r2=r1+30,sw=(i%2?1:0);
    rib+='<path d="M '+(-r1)+' 0 A '+r1+' '+r1+' 0 0 '+sw+' '+r1+' 0 A '+r2+' '+r2+' 0 0 '+(sw?0:1)+' '+(-r1)+' 0 Z" '+
      'stroke="'+cols[i]+'" style="color:'+cols[i]+';animation-delay:'+(0.55+i*0.22).toFixed(2)+'s;transform:rotate('+(i*47)+'deg)"/>';
  }
  document.getElementById('brib').innerHTML=rib;
  startParticles();
}

/* Poussière de vibranium aspirée vers le noyau puis relâchée par
   l'onde de choc. */
function startParticles(){
  try{
    const c=document.getElementById('bpart');
    if(!c||typeof c.getContext!=='function')return;
    const x=c.getContext('2d');if(!x)return;
    let W,H;
    function rs(){W=c.width=c.offsetWidth||window.innerWidth;H=c.height=c.offsetHeight||window.innerHeight;}
    rs();window.addEventListener('resize',rs);
    const P=[];
    for(let i=0;i<120;i++){
      const a=Math.random()*6.28,d=140+Math.random()*420;
      P.push({a:a,d:d,d0:d,sp:0.5+Math.random()*1.1,r:0.5+Math.random()*1.6,
              hue:Math.random()<0.3?'104,224,214':'203,164,245',ph:Math.random()*6.28});
    }
    const t0=Date.now();
    (function loop(){
      try{
        const el=Date.now()-t0;
        x.clearRect(0,0,W,H);
        const cx=W/2,cy=H*0.46;
        P.forEach(function(p){
          if(el<2600)p.d=Math.max(14,p.d-p.sp*(1+el/1400));   // aspiration
          else p.d+=p.sp*7;                                    // dispersion
          p.a+=0.0016*(1+(600-Math.min(p.d,600))/600);
          p.ph+=0.05;
          const px=cx+Math.cos(p.a)*p.d, py=cy+Math.sin(p.a)*p.d;
          const near=1-Math.min(1,p.d/p.d0);
          const al=Math.max(0,(el<2600?0.25+near*0.7:Math.max(0,1-(el-2600)/1100))*(0.6+0.4*Math.sin(p.ph)));
          x.beginPath();
          x.fillStyle='rgba('+p.hue+','+al.toFixed(3)+')';
          x.arc(px,py,p.r*(1+near*1.2),0,6.28);
          x.fill();
        });
        if(el<6000)requestAnimationFrame(loop);
      }catch(e){}
    })();
  }catch(e){}
  /* titre : chaque lettre naît en glyphe puis bascule en latin */
  const word='NDABA';
  const bt=document.getElementById('bt');
  bt.innerHTML=Array.from(word).map(function(c,i){
    return '<span class="ch" style="animation-delay:'+(1.45+i*0.11).toFixed(2)+'s">'+gly(c)+'</span>';
  }).join('');
  Array.from(word).forEach(function(c,i){
    setTimeout(function(){
      const el=bt.children[i];
      if(el){el.textContent=c;el.classList.add('lock');}
    },2050+i*110);
  });
}

/* ================= DÉMARRAGE ================= */
let bootT0=Date.now();
let entered=false;
function enterApp(){
  if(entered)return;
  entered=true;
  entryChime();
  const fl=document.getElementById('bflash');
  if(fl)fl.classList.add('go');
  const ir=document.getElementById('biris');
  if(ir)ir.classList.add('go');
  const app=document.getElementById('app');
  setTimeout(function(){
    document.getElementById('boot').classList.add('gone');
    app.style.display='';
    app.classList.add('arriving');
    render();
    setTimeout(function(){app.classList.remove('arriving');},1100);
  },300);
}
(async function start(){
  bootT0=Date.now();
  buildIntro();
  armSound();
  /* L'emblème s'embrase au moment où le noyau se verrouille. */
  setTimeout(function(){
    const l=document.querySelector('.blogo');
    if(l)l.classList.add('bloom');
  },2050);
  const bs=document.getElementById('bs');
  await loadIndex();
  bs.textContent=IDX.users.length
    ? 'Réseau vivant · '+IDX.users.length+' compte(s) · '+IDX.posts.length+' publication(s)'
    : 'Réseau vierge · soyez le premier compte';
  await loadSession();
  if(SES.current)ME=await getUser(SES.current);
  /* La séquence ne débouche plus sur une entrée automatique : une
     fois les couches refermées, la scène attend un geste. */
  setTimeout(function(){
    const b=document.getElementById('boot');
    if(b)b.classList.add('ready');
  },3200);
})();
const doorEl=document.getElementById('benter');
doorEl.addEventListener('click',function(e){
  e.stopPropagation();
  if(document.getElementById('boot').classList.contains('ready'))enterApp();
});
doorEl.addEventListener('keydown',function(e){
  if(e.key==='Enter'||e.key===' '){
    e.preventDefault();
    if(document.getElementById('boot').classList.contains('ready'))enterApp();
  }
});
document.getElementById('bsnd').addEventListener('click',function(e){
  e.stopPropagation();
  sndOn=!sndOn;
  this.classList.toggle('off',!sndOn);
  this.classList.remove('pending');
  if(sndOn&&!sndDone)playIgnition((Date.now()-bootT0)/1000);
  if(!sndOn&&actx){try{actx.suspend();}catch(err){}}
  else if(sndOn&&actx){try{actx.resume();}catch(err){}}
});

/* ================= POUSSIÈRE ================= */
(function dust(){
  try{
    const c=document.getElementById('dust');if(!c||typeof c.getContext!=='function')return;
    const x=c.getContext('2d');if(!x)return;
    let W,H;const ps=[];
    function rs(){W=c.width=innerWidth;H=c.height=innerHeight;}
    rs();addEventListener('resize',rs);
    for(let i=0;i<46;i++)ps.push({x:Math.random()*W,y:Math.random()*H,r:.4+Math.random()*1.3,s:.05+Math.random()*.22,a:.08+Math.random()*.4,t:Math.random()*6.28,v:Math.random()<.3});
    (function loop(){
      try{
        x.clearRect(0,0,W,H);
        ps.forEach(function(p){
          p.y-=p.s;p.t+=.02;
          if(p.y<-8){p.y=H+8;p.x=Math.random()*W;}
          const a=p.a*(.55+.45*Math.sin(p.t));
          x.beginPath();
          x.fillStyle=p.v?'rgba(104,224,214,'+a+')':'rgba(203,164,245,'+a+')';
          x.arc(p.x,p.y,p.r,0,6.28);x.fill();
        });
        requestAnimationFrame(loop);
      }catch(e){}
    })();
  }catch(e){}
})();

})();
</script>
</body>
</html>
