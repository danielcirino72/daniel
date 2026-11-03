[index.html](https://github.com/user-attachments/files/34341978/index.html)
<!doctype html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>O Último Sinal: Plataforma Zero</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Special+Elite&display=swap');
:root{--bg:#090a0d;--panel:#111319;--line:#343943;--ink:#e7e7e7;--muted:#9da3ad;--red:#b52b36;--glow:#7f1721}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(ellipse at 50% 15%,#20232b 0,#090a0d 60%);color:var(--ink);font-family:'Share Tech Mono',monospace;min-height:100vh}
body:after{content:"";position:fixed;inset:0;pointer-events:none;opacity:.12;background:repeating-linear-gradient(0deg,transparent 0 3px,#fff 4px,transparent 5px);mix-blend-mode:soft-light}
.wrap{max-width:920px;margin:auto;padding:24px 18px 50px}.top{display:flex;justify-content:space-between;gap:12px;align-items:center;border-bottom:1px solid var(--line);padding-bottom:12px;color:var(--muted);font-size:12px;letter-spacing:2px}
.logo{color:#d7d7d7}.status{color:#d04b54}.hero{margin:22px 0 16px;border:1px solid #444;background:linear-gradient(135deg,#151820,#08090c);min-height:185px;display:flex;align-items:end;padding:22px;position:relative;overflow:hidden}
.hero:before{content:"";position:absolute;inset:0;background:linear-gradient(90deg,rgba(0,0,0,.1),rgba(0,0,0,.7)),repeating-linear-gradient(90deg,transparent 0 70px,rgba(255,255,255,.025) 71px 72px);opacity:.8}
.hero:after{content:"";position:absolute;left:0;right:0;bottom:0;height:2px;background:var(--red);box-shadow:0 0 18px var(--red)}
.heroInner{position:relative;z-index:1}.eyebrow{color:#d34b55;font-size:12px;letter-spacing:4px}.title{font-family:'Special Elite',serif;font-size:clamp(32px,7vw,58px);line-height:1;margin:9px 0;text-shadow:2px 2px #4d1017}.subtitle{color:#aeb3bd;font-size:13px}
.panel{border:1px solid var(--line);background:rgba(15,17,22,.94);padding:clamp(18px,4vw,30px);box-shadow:0 18px 55px #0008}
.meta{display:flex;justify-content:space-between;gap:12px;color:var(--muted);font-size:12px;border-bottom:1px solid #292d35;padding-bottom:12px;margin-bottom:20px}
.sceneTitle{font-family:'Special Elite',serif;font-size:24px;color:#fff;margin:0 0 18px}
.art{height:125px;margin:0 0 20px;border:1px solid #30343d;position:relative;overflow:hidden;background:linear-gradient(180deg,#111720,#090a0e)}
.art.station{background:linear-gradient(180deg,#151922 0%,#08090d 75%),repeating-linear-gradient(90deg,transparent 0 70px,#353944 71px 73px)}
.art.train{background:linear-gradient(90deg,#090a0e,#262a33 50%,#090a0e)}
.art.archive{background:repeating-linear-gradient(90deg,#171a20 0 42px,#252a33 43px 45px)}
.art:before{content:"";position:absolute;left:0;right:0;bottom:25px;height:2px;background:#747b87;box-shadow:0 0 14px #aeb6c5}
.art:after{content:"";position:absolute;left:12%;right:12%;bottom:0;height:25px;background:repeating-linear-gradient(90deg,#252a32 0 30px,#090a0e 31px 48px);clip-path:polygon(0 0,100% 0,88% 100%,12% 100%)}
.art .light{position:absolute;top:18px;left:48%;width:80px;height:5px;background:#d7d8d8;box-shadow:0 0 35px 12px #aab4c866}
.dialogue{font-family:'Special Elite',serif;font-size:18px;line-height:1.65;white-space:pre-line;min-height:190px}
.dialogue .speaker{font-family:'Share Tech Mono',monospace;font-size:12px;letter-spacing:2px;color:#d34b55;display:block;margin:18px 0 5px}
.dialogue p{margin:0 0 13px}
.choices{display:grid;gap:10px;margin-top:24px}
button{font:inherit;color:var(--ink);cursor:pointer}
.choice,.control{background:#171a21;border:1px solid #454b56;padding:14px 16px;text-align:left;transition:.18s}
.choice:hover,.control:hover{border-color:#c13b47;background:#21171b;transform:translateY(-1px)}
.choice small{display:block;color:#9299a4;margin-top:5px;font-size:11px}
.controls{display:flex;gap:10px;flex-wrap:wrap;margin-top:20px}
.control{font-size:12px;letter-spacing:1px;padding:10px 13px}
.footer{display:flex;justify-content:space-between;color:#727985;font-size:11px;margin-top:15px;gap:10px}
.hidden{display:none!important}.red{color:#d34b55}.ending{border:1px solid #743039;padding:18px;margin:15px 0;background:#180f13}
input{accent-color:#b52b36}
@media(max-width:600px){.top{font-size:10px}.hero{min-height:150px}.dialogue{font-size:16px}.meta{font-size:10px}}
</style>
</head>
<body>
<div class="wrap">
 <div class="top"><div class="logo">KUROTSUKI / ARQUIVO 017</div><div class="status" id="clock">03:17 — SEM SINAL</div></div>
 <section class="hero"><div class="heroInner"><div class="eyebrow">UMA VISUAL NOVEL DE TERROR PSICOLÓGICO</div><div class="title">PLATAFORMA ZERO</div><div class="subtitle">Algumas lembranças não querem ser encontradas.</div></div></section>
 <main class="panel">
  <div class="meta"><span id="chapter">PRÓLOGO</span><span id="progress">ARQUIVO 01 / 06</span></div>
  <div class="art station" id="art"><span class="light"></span></div>
  <h1 class="sceneTitle" id="sceneTitle">03:17</h1>
  <div class="dialogue" id="dialogue"></div>
  <div class="choices" id="choices"></div>
  <div class="controls">
   <button class="control" id="restart">↻ RECOMEÇAR</button>
   <button class="control" id="history">▤ HISTÓRICO</button>
   <button class="control" id="sound">♫ SOM: DESLIGADO</button>
  </div>
  <div class="footer"><span>Suas escolhas alteram as lembranças e os finais.</span><span>REN'PY-INSPIRED / HTML EDITION</span></div>
 </main>
</div>
<script>
const $=id=>document.getElementById(id);
let state={scene:'prologue',yui:false,akane:false,record:false,trust:false,confront:false,door:'',history:[],sound:false};
const scenes={
prologue:{chapter:'PRÓLOGO',progress:'01 / 06',title:'03:17 — O ARQUIVO',art:'station',text:[
['NARRAÇÃO','A chuva bate na janela. Renji Takahashi está sozinho diante do computador. Sobre a mesa: fotografias antigas, documentos policiais e um gravador que ele não se lembra de ter ligado.'],
['RENJI','Eu já vi esse arquivo...'],
['NARRAÇÃO','Na tela, uma pasta aparece aberta: CASO_017. O relógio muda para 03:17. Três batidas soam na porta.'],
['SISTEMA','MENSAGEM RECEBIDA — YUI NAKAMURA: “Você prometeu que voltaria. Eu ainda estou esperando.”'],
['RENJI','Não. Yui morreu há treze anos.'],
['KURODA','Takahashi, escute com atenção. Não vá até a estação. Eu também recebi a mensagem.'],
['NARRAÇÃO','A ligação cai. Na tela surge outra frase: ELE ESTÁ MENTINDO.']
],choices:[['Ir até a estação Kurotsuki','O arquivo indica uma localização.','station'],['Ligar novamente para Kuroda','Talvez ele saiba mais do que está dizendo.','call'],['Examinar a fotografia de Yui','Uma anotação foi escrita no verso.','photo']]},
call:{chapter:'PRÓLOGO',progress:'01 / 06',title:'A LIGAÇÃO',art:'archive',text:[
['RENJI','Kuroda, o que aconteceu naquela noite?'],
['KURODA','Você não devia estar ouvindo essa mensagem.'],
['RENJI','Então por que meu nome está no arquivo?'],
['KURODA','Porque você foi a última pessoa a vê-la viva. E porque há coisas que não devem ser lembradas.'],
['NARRAÇÃO','Antes que Renji responda, a ligação se enche de estática. Uma voz infantil sussurra: “Plataforma zero”.']
],choices:[['Ir até a estação','Não há mais como ignorar o chamado.','station']]},
photo:{chapter:'PRÓLOGO',progress:'01 / 06',title:'A FOTOGRAFIA',art:'archive',text:[
['NARRAÇÃO','No verso da fotografia está escrito: “Para Renji. Não se esqueça de mim.” A tinta parece recente.'],
['RENJI','Quem escreveu isso?'],
['NARRAÇÃO','Uma segunda frase surge lentamente, como se alguém escrevesse do outro lado do papel: “Você estava no trem.”']
],choices:[['Ir até a estação','A resposta está em Kurotsuki.','station']]},
station:{chapter:'CAPÍTULO 1',progress:'02 / 06',title:'A ESTAÇÃO QUE NÃO EXISTE',art:'station',text:[
['NARRAÇÃO','03:42. A estação Kurotsuki está abandonada há anos. A chuva atravessa o teto quebrado. Apenas uma plataforma permanece iluminada.'],
['YUI','Renji? Você demorou.'],
['RENJI','Yui?! Isso não é possível.'],
['YUI','Você sempre diz isso. Então por que ainda consegue me ouvir?'],
['NARRAÇÃO','As luzes apagam. Quando retornam, Yui desapareceu. No chão há um gravador.'],
['GRAVAÇÃO DE YUI','Se você estiver ouvindo isso, não confie no homem de uniforme.'],
['GRAVAÇÃO DE RENJI','Eu sei. Ela precisa morrer novamente.'],
['RENJI','Essa é a minha voz...']
],choices:[['Descer para a Plataforma Zero','A porta metálica está aberta.','platform'],['Procurar Akane antes de descer','Uma mensagem dela aparece no celular.','akane'],['Fugir da estação','A saída parece mais distante do que antes.','flee']]},
akane:{chapter:'CAPÍTULO 1',progress:'02 / 06',title:'A MENSAGEM DE AKANE',art:'station',text:[
['AKANE','Renji, não desça. Eu estou vendo você.'],
['RENJI','Onde você está?'],
['AKANE','Não olha para trás.'],
['NARRAÇÃO','Renji sente uma respiração junto à nuca. Uma voz idêntica à de Yui sussurra: “Você vai olhar mesmo assim?”'],
['RENJI','Akane... eu vou encontrar você.']
],choices:[['Descer para a Plataforma Zero','A escadaria parece não ter fim.','platform']]},
flee:{chapter:'CAPÍTULO 1',progress:'02 / 06',title:'A SAÍDA',art:'station',text:[
['NARRAÇÃO','Renji corre até a saída. A placa indica RUA PRINCIPAL, mas a porta se abre para a mesma plataforma.'],
['RENJI','Não... eu acabei de passar por aqui.'],
['YUI','Você sempre tenta fugir primeiro.'],
['NARRAÇÃO','Uma porta se abre sob a placa PLATAFORMA 0. Não há outro caminho.']
],choices:[['Entrar na Plataforma Zero','O ar que vem da escadaria é gelado.','platform']]},
platform:{chapter:'CAPÍTULO 2',progress:'03 / 06',title:'O PASSAGEIRO',art:'train',text:[
['NARRAÇÃO','04:03. A Plataforma Zero parece não ter fim. Fotografias de pessoas desaparecidas pendem do teto. Todas têm os olhos riscados.'],
['MIZUKI','Você conhece esta menina?'],
['RENJI','Yui... Quem é você?'],
['MIZUKI','Mizuki Nakamura. A mãe dela. Você sabe por que minha filha morreu?'],
['RENJI','Foi um acidente ferroviário.'],
['MIZUKI','Um acidente? Então por que você estava no trem?'],
['NARRAÇÃO','Uma dor atravessa a cabeça de Renji. Uma cabine. Uma criança chorando. Uma porta sendo trancada.'],
['KURODA','Afaste-se dela!'],
['NARRAÇÃO','Kuroda surge com uma arma. Um disparo ecoa. Quando a luz retorna, Mizuki desapareceu. A fotografia em suas mãos mostra Renji sorrindo com os olhos completamente negros.']
],choices:[['Confiar em Kuroda','Ele diz que pode explicar o arquivo.','trust'],['Acusar Kuroda','Exija saber o que aconteceu no trem.','accuse'],['Destruir o arquivo','Talvez as lembranças sejam a armadilha.','destroy']]},
trust:{chapter:'CAPÍTULO 3',progress:'04 / 06',title:'A CONFISSÃO',art:'archive',text:[
['KURODA','Eu era o maquinista naquela noite. Tentei impedir o que aconteceu.'],
['RENJI','Você matou todos?'],
['KURODA','Não. Havia uma quarta pessoa no trem.'],
['RENJI','Quem?'],
['NARRAÇÃO','Kuroda mostra uma gravação. Renji aparece sozinho numa sala, falando com uma cadeira vazia.'],
['SISTEMA','O PASSAGEIRO NÚMERO QUATRO NUNCA EXISTIU.'],
['KURODA','A gravação pode libertar Yui. Mas você precisa lembrar o que fez.']
],choices:[['Assistir à gravação completa','Renji precisa encarar a memória.','memory']]},
accuse:{chapter:'CAPÍTULO 3',progress:'04 / 06',title:'O HOMEM DE UNIFORME',art:'archive',text:[
['RENJI','Você encobriu tudo. Você matou aquelas pessoas!'],
['KURODA','Eu assinei o relatório. Sim. Mas não fui eu que fechou a porta.'],
['RENJI','Quem foi?'],
['KURODA','Você precisa lembrar.'],
['NARRAÇÃO','Kuroda entrega uma fita. Na etiqueta: ÚLTIMOS 13 SEGUNDOS.']
],choices:[['Reproduzir a fita','O ruído revela uma voz conhecida.','memory']]},
destroy:{chapter:'CAPÍTULO 3',progress:'04 / 06',title:'CINZAS',art:'archive',text:[
['NARRAÇÃO','Renji rasga o arquivo. As folhas viram cinzas antes de tocar o chão.'],
['RENJI','Acabou.'],
['YUI','Você sempre destrói as provas quando sente medo.'],
['NARRAÇÃO','O reflexo de Renji no vidro continua sorrindo, mesmo quando ele para.']
],choices:[['Seguir a voz de Yui','Não há mais documentos. Só lembranças.','memory']]},
memory:{chapter:'CAPÍTULO 4',progress:'05 / 06',title:'O QUARTO PASSAGEIRO',art:'train',text:[
['NARRAÇÃO','Renji desperta dentro de um trem. Yui está sentada à sua frente, exatamente como na fotografia.'],
['YUI','Você lembra agora?'],
['RENJI','Eu estava no trem. Você também. Akane estava lá.'],
['YUI','E o que aconteceu?'],
['NARRAÇÃO','A lembrança retorna: Kuroda tenta abrir as portas. Yui chora. Akane chama por Renji. No último vagão, uma figura idêntica a ele sorri.'],
['AKANE','Não é você!'],
['QUARTO PASSAGEIRO','É claro que sou.'],
['YUI','Você precisa escolher. Só um de vocês pode sair.']
],choices:[['Salvar Yui','Renji segura a mão da menina.','saveYui'],['Procurar Akane','Uma segunda porta se abre no vagão.','saveAkane'],['Enfrentar o quarto passageiro','A criatura parece ter medo de Renji.','fight']]},
saveYui:{chapter:'CAPÍTULO 4',progress:'05 / 06',title:'A MÃO DE YUI',art:'train',text:[
['NARRAÇÃO','Renji segura a mão de Yui. A figura grita. Uma lembrança da menina permanece com ele.'],
['YUI','Você prometeu que voltaria.'],
['RENJI','Eu estou aqui. Desta vez, não vou soltar.']
],choices:[['Continuar','O trem para. A estação está vazia.','last']]},
saveAkane:{chapter:'CAPÍTULO 4',progress:'05 / 06',title:'A SEGUNDA PORTA',art:'train',text:[
['NARRAÇÃO','Akane aparece do outro lado da porta. Ela parece mais velha, mas seus olhos são os mesmos.'],
['AKANE','Eu esperei por você. Mas, para me levar, precisa deixar Yui para trás.'],
['RENJI','Eu não posso escolher entre vocês.'],
['AKANE','Você já escolheu uma vez.']
],choices:[['Escolher Akane','Renji atravessa a porta.','lastAkane'],['Voltar para Yui','A porta começa a se fechar.','last']]},
fight:{chapter:'CAPÍTULO 4',progress:'05 / 06',title:'O ORIGINAL',art:'train',text:[
['RENJI','Você não é eu.'],
['QUARTO PASSAGEIRO','Eu sou a parte que você apagou. A parte que queria viver.'],
['NARRAÇÃO','Renji avança. A criatura recua, chorando. Por um instante, os dois compartilham a mesma lembrança.'],
['QUARTO PASSAGEIRO','Eu só queria viver.'],
['RENJI','Eu também.']
],choices:[['Continuar até a estação','Uma luz branca cobre o vagão.','last']]},
lastAkane:{chapter:'CAPÍTULO FINAL',progress:'06 / 06',title:'A IRMÃ',art:'station',text:[
['NARRAÇÃO','Renji atravessa a porta com Akane. O trem parte. Yui fica na plataforma, segurando a fotografia.'],
['AKANE','Agora podemos ir para casa?'],
['RENJI','Podemos.'],
['NARRAÇÃO','No painel da estação aparece CASO 018 — ABERTO. Kuroda recebe uma nova ligação.']
],choices:[['Ver o desfecho','A estação começa a desaparecer.','endingBad']]},
last:{chapter:'CAPÍTULO FINAL',progress:'06 / 06',title:'A ÚLTIMA PORTA',art:'station',text:[
['NARRAÇÃO','A estação está vazia. Três portas aparecem: ESQUECER, VOLTAR e LEMBRAR. O telefone toca.'],
['KURODA','Você precisa me dizer o que aconteceu.'],
['RENJI','Eu me lembrei. Você nunca tentou salvar ninguém, não é?'],
['YUI','Renji... não confie nele.'],
['NARRAÇÃO','Uma mensagem aparece: “Você já escolheu uma vez. Escolha novamente.”']
],choices:[['Porta 01 — Esquecer','Deixar tudo para trás.','doorForget'],['Porta 02 — Voltar','Aceitar a partida.','doorReturn'],['Porta 03 — Lembrar','Encarar o que realmente aconteceu.','doorRemember']]},
doorForget:{chapter:'EPÍLOGO',progress:'FINAL',title:'O ESQUECIDO',art:'archive',ending:'bad',text:[
['NARRAÇÃO','Renji atravessa a primeira porta. Acorda em sua cama. São 08:00. O sol entra pela janela.'],
['RENJI','Que sonho estranho...'],
['NARRAÇÃO','Uma fotografia está sobre a mesa. Ele não reconhece ninguém. O telefone toca.'],
['VOZ FEMININA','Você esqueceu de novo.'],
['NARRAÇÃO','No reflexo da janela, uma menina está parada atrás dele.']
]},
doorReturn:{chapter:'EPÍLOGO',progress:'FINAL',title:'A ÚLTIMA PARTIDA',art:'train',ending:'tragic',text:[
['NARRAÇÃO','Renji atravessa a segunda porta. O trem parte. Yui está sentada ao seu lado.'],
['YUI','Agora podemos ir para casa?'],
['RENJI','Podemos.'],
['NARRAÇÃO','Na plataforma, Kuroda observa o trem desaparecer. Seu telefone toca: CASO 018 — ABERTO.']
]},
doorRemember:{chapter:'EPÍLOGO',progress:'FINAL',title:'MEMÓRIAS DE CINZAS',art:'train',ending:'secret',text:[
['NARRAÇÃO','Renji escolhe lembrar. Todas as memórias retornam. A figura surge atrás dele.'],
['QUARTO PASSAGEIRO','Obrigado por guardar minhas lembranças.'],
['RENJI','Quem é você?'],
['QUARTO PASSAGEIRO','O original.'],
['NARRAÇÃO','A tela escurece. A fotografia de Renji aparece com seu nome riscado.']
]},
endingTrue:{chapter:'EPÍLOGO',progress:'FINAL SECRETO',title:'O ÚLTIMO SINAL',art:'station',ending:'true',text:[
['NARRAÇÃO','Renji não atravessa nenhuma porta. Ele se vira para o quarto passageiro.'],
['QUARTO PASSAGEIRO','Você não pode ficar.'],
['RENJI','Eu sei.'],
['QUARTO PASSAGEIRO','Então por que continua tentando?'],
['RENJI','Porque prometi que voltaria.'],
['NARRAÇÃO','A criatura avança. Renji segura sua mão. Pela primeira vez, ela chora.'],
['QUARTO PASSAGEIRO','Eu só queria viver.'],
['RENJI','Eu também.'],
['NARRAÇÃO','Uma luz branca cobre a estação. Quando desaparece, Yui está sozinha. O relógio marca 03:18.'],
['YUI','Obrigada, Renji.'],
['NARRAÇÃO','Dez anos depois, Akane atende o telefone numa estação reconstruída.'],
['RENJI','Akane... você ainda se lembra de mim?'],
['NARRAÇÃO','Ela começa a chorar. Três batidas ecoam. O trem chegou ao destino.']
]}
};
function render(id){
 state.scene=id;const s=scenes[id];$('chapter').textContent=s.chapter;$('progress').textContent=s.progress;$('sceneTitle').textContent=s.title;$('art').className='art '+(s.art||'station');$('clock').textContent=id.startsWith('door')||id.startsWith('ending')?'03:18 — SINAL RESTAURADO':'03:17 — SEM SINAL';
 $('dialogue').innerHTML='';$('choices').innerHTML='';
 s.text.forEach(([who,line])=>{const span=document.createElement('span');span.className='speaker';span.textContent=who;const p=document.createElement('p');p.textContent=line;$('dialogue').append(span,p);});
 if(s.ending){
   const label=document.createElement('div');label.className='ending';label.innerHTML='<strong class="red">'+({true:'FINAL VERDADEIRO',bad:'FINAL RUIM',tragic:'FINAL TRÁGICO',secret:'FINAL ALTERNATIVO'}[s.ending])+'</strong><p>FIM — O ÚLTIMO SINAL: PLATAFORMA ZERO</p>'; $('choices').append(label);
   if(s.ending==='secret' && state.yui && state.record && state.confront){const b=mk('Desbloquear o final verdadeiro','Você reuniu as lembranças necessárias.','endingTrue');$('choices').append(b);}
   const again=mk('Jogar novamente','Suas escolhas serão reiniciadas.','restart');$('choices').append(again);return;
 }
 (s.choices||[]).forEach(([label,desc,next])=>$('choices').append(mk(label,desc,next)));
}
function mk(label,desc,next){const b=document.createElement('button');b.className='choice';b.innerHTML='<span>'+label+'</span><small>'+desc+'</small>';b.onclick=()=>choose(next);return b}
function choose(next){
 state.history.push(state.scene);
 if(next==='trust'){state.trust=true;state.record=true}
 if(next==='accuse'){state.record=true}
 if(next==='destroy'){state.record=false}
 if(next==='saveYui'){state.yui=true}
 if(next==='saveAkane'){state.akane=true}
 if(next==='fight'){state.confront=true}
 if(next==='doorRemember'){
   if(state.yui&&state.record&&state.confront){render('endingTrue');return}
   render('doorRemember');return
 }
 if(next==='last' && state.yui && state.record && state.confront){render('last');return}
 if(next==='last' && state.yui){state.confront=true}
 if(next==='endingBad'){render('doorReturn');return}
 if(next==='restart'){reset();return}
 render(next);
}
function reset(){state={scene:'prologue',yui:false,akane:false,record:false,trust:false,confront:false,door:'',history:[],sound:false};render('prologue')}
$('restart').onclick=reset;
$('history').onclick=()=>{if(!state.history.length){alert('Ainda não há cenas anteriores.');return}alert('Cenas visitadas:\\n'+state.history.map(x=>scenes[x].title).join('\\n'))};
$('sound').onclick=()=>{state.sound=!state.sound;$('sound').textContent='♫ SOM: '+(state.sound?'LIGADO':'DESLIGADO');alert('Esta versão usa trilha sonora desligada por padrão. Você pode ativar os sons do navegador para efeitos do jogo.')};
render('prologue');
</script>
</body>
</html>
