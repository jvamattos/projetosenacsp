<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Escolha seu Futuro</title>
<style>
:root{
  --bg:#07090d; --bg2:#0d1117; --card:#121820; --line:#1f2733;
  --txt:#e8edf4; --dim:#8a97a8; --accent:#3ddc97; --accent2:#e8b64c; --warn:#e85d5d;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
*{box-sizing:border-box}
html{height:100%;scroll-padding-top:env(safe-area-inset-top,0px)}
body{height:100%;margin:0;background:radial-gradient(1200px 800px at 50% -10%,#0f1621,var(--bg));color:var(--txt);
  font-family:'Segoe UI',system-ui,-apple-system,sans-serif;overflow-x:hidden;min-height:100vh}
#app{max-width:720px;margin:0 auto;min-height:100vh;display:flex;flex-direction:column;padding:28px 20px 40px}
.eyebrow{font-size:13px;color:var(--accent);letter-spacing:.04em;margin-bottom:6px}
.timeline{display:flex;gap:6px;font-size:11px;color:var(--dim);margin-bottom:22px;flex-wrap:wrap}
.timeline b{color:var(--accent)}
.stage{flex:1;display:flex;flex-direction:column;justify-content:center;animation:fade .5s ease}
@keyframes fade{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
.big{font-size:clamp(28px,7vw,44px);font-weight:700;line-height:1.15;margin:10px 0}
.line{font-size:18px;line-height:1.6;color:var(--txt);margin:8px 0;min-height:1em}
.lead{font-size:15px;color:var(--dim);margin-bottom:18px}
.tag{display:inline-block;font-size:11px;color:var(--accent2);border:1px solid #4a3d1f;background:#1a1509;
  padding:3px 9px;border-radius:20px;margin-bottom:14px}
.btnrow{display:flex;gap:10px;flex-wrap:wrap;margin-top:22px}
button.primary{background:var(--accent);color:#04170f;border:none;padding:13px 24px;border-radius:10px;
  font-size:15px;font-weight:600;cursor:pointer}
button.primary:disabled{opacity:.4;cursor:default}
button.ghost{background:transparent;color:var(--txt);border:1px solid var(--line);padding:12px 20px;
  border-radius:10px;font-size:14px;cursor:pointer}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:10px;margin:14px 0}
.opt{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:14px 12px;cursor:pointer;
  text-align:left;transition:border-color .15s,transform .15s}
.opt:hover{border-color:var(--accent);transform:translateY(-2px)}
.opt.sel{border-color:var(--accent);background:#0e1e18}
.opt .em{font-size:22px;display:block;margin-bottom:6px}
.opt .t{font-size:14px;font-weight:600}
.choices{display:flex;flex-direction:column;gap:8px;margin-top:18px}
.choice{background:var(--card);border:1px solid var(--line);border-radius:10px;padding:13px 15px;
  cursor:pointer;font-size:14.5px;text-align:left}
.choice:hover{border-color:var(--accent)}
.result{border-left:3px solid var(--accent);padding:14px 16px;background:var(--card);border-radius:8px;margin:16px 0}
.result.warn{border-color:var(--warn)}
.result.gold{border-color:var(--accent2)}
.result h3{margin:0 0 6px;font-size:17px}
.diagram{font-family:monospace;font-size:13px;color:var(--accent);line-height:2;white-space:pre;margin:16px 0}
.scenarios{display:grid;gap:10px;margin:16px 0}
.sc{border:1px solid var(--line);border-radius:10px;padding:13px 15px;background:var(--card)}
.sc b{color:var(--accent2)}
.summary-row{display:flex;justify-content:space-between;border-bottom:1px solid var(--line);
  padding:9px 0;font-size:14px}
.summary-row span:first-child{color:var(--dim)}
.progressbar{height:3px;background:var(--line);border-radius:2px;margin-bottom:20px;overflow:hidden}
.progressbar i{display:block;height:100%;background:var(--accent);transition:width .4s}
</style>
</head>
<body>
<div id="app"></div>
<script>
const $=id=>document.getElementById(id);
const app=document.getElementById('app');

const AREAS={
 'Tecnologia':{em:'💻',profs:['Desenvolvedor de software','Especialista em cibersegurança','Analista de dados','Desenvolvedor de jogos','Engenheiro de IA'],tasks:['gerar código automaticamente','encontrar erros e vulnerabilidades','escrever documentação','criar testes','montar protótipos rápidos']},
 'Saúde':{em:'⚕️',profs:['Médico','Enfermeiro','Psicólogo','Fisioterapeuta','Técnico de enfermagem'],tasks:['triagem inicial de sintomas','análise de exames e imagens','organização de prontuários','sugestão de diagnósticos','monitoramento remoto de pacientes']},
 'Direito':{em:'⚖️',profs:['Advogado','Analista jurídico','Promotor','Juiz','Consultor jurídico'],tasks:['pesquisa de jurisprudência','revisão de contratos','redação de peças simples','resumo de processos','análise de risco jurídico']},
 'Design e criação':{em:'🎨',profs:['Designer','Editor de vídeo','Publicitário','Fotógrafo','Criador de conteúdo'],tasks:['gerar imagens e variações','montar layouts','editar vídeo automaticamente','criar roteiros','prototipar campanhas']},
 'Administração e negócios':{em:'💼',profs:['Administrador','Empreendedor','RH','Consultor','Gerente'],tasks:['triagem de currículos','organização de planilhas','relatórios automáticos','previsões simples','atendimento inicial a clientes']},
 'Finanças':{em:'💰',profs:['Contador','Analista financeiro','Economista','Auditor','Consultor financeiro'],tasks:['conciliação de dados','detecção de fraudes','projeções financeiras','geração de relatórios','análise de risco']},
 'Indústria':{em:'🏭',profs:['Operador','Técnico','Mecânico','Supervisor','Engenheiro de produção'],tasks:['operação de máquinas repetitivas','controle de qualidade visual','manutenção preditiva','logística interna','monitoramento de linha']},
 'Educação':{em:'📚',profs:['Professor','Coordenador','Pesquisador','Tutor','Produtor de conteúdo educacional'],tasks:['correção automática','geração de exercícios','tutoria personalizada','resumo de conteúdos','planejamento de aulas']},
 'Comunicação e marketing':{em:'📢',profs:['Jornalista','Social media','Copywriter','Relações públicas','Especialista em marketing'],tasks:['redação de textos curtos','geração de posts','análise de métricas','tradução e adaptação','pesquisa de pauta']},
 'Ciência e pesquisa':{em:'🔬',profs:['Cientista de dados','Biólogo','Físico','Pesquisador acadêmico','Analista de laboratório'],tasks:['análise de grandes volumes de dados','simulações','revisão de literatura','organização de experimentos','geração de hipóteses']},
 'Transporte e logística':{em:'🚚',profs:['Motorista','Caminhoneiro','Operador logístico','Gestor de logística','Piloto'],tasks:['roteirização automática','monitoramento de frota','previsão de demanda','condução assistida','gestão de estoque']},
 'Engenharia':{em:'🏗️',profs:['Engenheiro civil','Engenheiro mecânico','Engenheiro elétrico','Arquiteto','Técnico especializado'],tasks:['cálculos estruturais','simulações de projeto','geração de plantas','detecção de falhas','otimização de materiais']},
 'Comércio e atendimento':{em:'🛒',profs:['Vendedor','Caixa','Atendente','Gerente de loja','Representante comercial'],tasks:['atendimento inicial automatizado','recomendação de produtos','controle de estoque','emissão de notas','análise de vendas']}
};

const TRAITS=[['🧠','Analítico'],['🎨','Criativo'],['🤝','Comunicativo'],['🔧','Prático'],['🚀','Empreendedor'],['❤️','Gosto de trabalhar com pessoas'],['💻','Gosto de tecnologia']];

let S={traits:[],area:null,prof:null,choices:[],stats:{adapt:0,humano:0,tecnico:0,tradicional:0}};

function bump(k,n){S.stats[k]=(S.stats[k]||0)+n}
function log(txt){S.choices.push(txt)}

const YEARS=['2026','2028','2031','2035','2040','FUTURO'];
function timelineHTML(active){
  return '<div class="timeline">'+YEARS.map(y=>`<span>${y===active?'<b>'+y+'</b>':y}</span>`).join(' → ')+'</div>';
}
function bar(pct){return `<div class="progressbar"><i style="width:${pct}%"></i></div>`;}

function render(node){app.innerHTML='';app.appendChild(node);window.scrollTo(0,0);}
function el(html){const d=document.createElement('div');d.className='stage';d.innerHTML=html;return d;}

// ---------- INTRO ----------
function screenIntro(){
  const lines=['2026','Você está entrando no mercado de trabalho.',
    'Durante as próximas décadas, máquinas e inteligências artificiais serão capazes de realizar cada vez mais tarefas.',
    'Você está preparado?'];
  let i=0;
  const n=el(`<div class="eyebrow">ESCOLHA SEU FUTURO</div><div id="ln" class="big"></div>
    <div class="btnrow"><button class="primary" id="go" style="display:none">COMEÇAR MINHA HISTÓRIA</button></div>`);
  render(n);
  const ln=n.querySelector('#ln'), go=n.querySelector('#go');
  function step(){ln.textContent=lines[i];i++;if(i<lines.length){setTimeout(step,1600);}else{go.style.display='inline-block';}}
  step();
  go.onclick=screenTraits;
}

// ---------- TRAITS ----------
function screenTraits(){
  const n=el(`${bar(10)}<div class="eyebrow">PERSONAGEM</div>
    <div class="big" style="font-size:26px">Qual dessas características mais combina com você?</div>
    <div class="lead">Escolha até duas.</div>
    <div class="grid" id="g"></div>
    <div class="btnrow"><button class="primary" id="next" disabled>Continuar</button></div>`);
  const g=n.querySelector('#g');
  TRAITS.forEach(([em,label])=>{
    const o=document.createElement('div');o.className='opt';
    o.innerHTML=`<span class="em">${em}</span><span class="t">${label}</span>`;
    o.onclick=()=>{
      if(o.classList.contains('sel')){o.classList.remove('sel');S.traits=S.traits.filter(t=>t!==label);}
      else{ if(S.traits.length>=2)return; o.classList.add('sel');S.traits.push(label);}
      n.querySelector('#next').disabled=S.traits.length===0;
    };
    g.appendChild(o);
  });
  render(n);
  n.querySelector('#next').onclick=screenArea;
}

// ---------- AREA ----------
function screenArea(){
  const n=el(`${bar(20)}<div class="eyebrow">18 ANOS</div>
    <div class="big" style="font-size:26px">Qual caminho profissional deseja seguir?</div>
    <div class="grid" id="g"></div>`);
  const g=n.querySelector('#g');
  Object.entries(AREAS).forEach(([name,d])=>{
    const o=document.createElement('div');o.className='opt';
    o.innerHTML=`<span class="em">${d.em}</span><span class="t">${name}</span>`;
    o.onclick=()=>{S.area=name;screenProf();};
    g.appendChild(o);
  });
  render(n);
}

function screenProf(){
  const d=AREAS[S.area];
  const n=el(`${bar(28)}<div class="eyebrow">${S.area}</div>
    <div class="big" style="font-size:26px">Escolha sua profissão.</div>
    <div class="grid" id="g"></div>`);
  const g=n.querySelector('#g');
  d.profs.forEach(p=>{
    const o=document.createElement('div');o.className='opt';
    o.innerHTML=`<span class="t">${p}</span>`;
    o.onclick=()=>{S.prof=p;screenContact();};
    g.appendChild(o);
  });
  render(n);
}

// ---------- 2028 CONTACT WITH AI ----------
function screenContact(){
  const d=AREAS[S.area];
  const tasks=d.tasks.slice(0,3).map(t=>'• '+t).join('<br>');
  const n=el(`${bar(38)}${timelineHTML('2028')}
    <div class="line">Ferramentas de inteligência artificial começam a executar parte das tarefas do seu trabalho como <b>${S.prof}</b>, como:</div>
    <div class="line" style="color:var(--dim);font-size:15px">${tasks}</div>
    <div class="line" style="margin-top:14px">O que você faz?</div>
    <div class="choices" id="c"></div>`);
  const opts=[
    ['Ignoro. Minha experiência é suficiente.',{tradicional:2}],
    ['Aprendo a utilizar IA como ferramenta.',{adapt:2,tecnico:1}],
    ['Faço uma especialização profissional.',{adapt:1,tecnico:2}],
    ['Tento migrar para uma função menos automatizável.',{humano:2}],
    ['Começo meu próprio negócio utilizando tecnologia.',{adapt:2,humano:1}],
    ['Aprendo profundamente como essas novas tecnologias funcionam.',{tecnico:3}]
  ];
  const c=n.querySelector('#c');
  opts.forEach(([txt,eff])=>{
    const b=document.createElement('div');b.className='choice';b.textContent=txt;
    b.onclick=()=>{Object.entries(eff).forEach(([k,v])=>bump(k,v));log('2028: '+txt);screenSecondEvent();};
    c.appendChild(b);
  });
  render(n);
}

// ---------- 2031 ----------
function screenSecondEvent(){
  const n=el(`${bar(48)}${timelineHTML('2031')}
    <div class="line">Uma nova geração de inteligência artificial consegue realizar tarefas que, poucos anos atrás, pareciam exclusivamente humanas.</div>
    <div class="line" style="color:var(--dim)">Uma tarefa que levava horas agora pode ser feita em minutos com auxílio de IA na área de ${S.area.toLowerCase()}.</div>
    <div class="choices" id="c"></div>`);
  const opts=[
    ['Utilizar a tecnologia no dia a dia.',{adapt:2,tecnico:1}],
    ['Continuar trabalhando da maneira tradicional.',{tradicional:2}],
    ['Aprender uma nova habilidade.',{adapt:1,humano:1}],
    ['Mudar de empresa.',{adapt:1}],
    ['Mudar parcialmente de carreira.',{humano:1,adapt:1}],
    ['Empreender.',{adapt:2,humano:1}],
    ['Especializar-se em atividades humanas.',{humano:3}],
    ['Estudar IA a fundo.',{tecnico:3}]
  ];
  const c=n.querySelector('#c');
  opts.forEach(([txt,eff])=>{
    const b=document.createElement('div');b.className='choice';b.textContent=txt;
    b.onclick=()=>{Object.entries(eff).forEach(([k,v])=>bump(k,v));log('2031: '+txt);screenPhysical();};
    c.appendChild(b);
  });
  render(n);
}

// ---------- 2035 PHYSICAL AUTOMATION ----------
function screenPhysical(){
  const n=el(`${bar(60)}${timelineHTML('2035')}
    <div class="line">Agora não é apenas software. Robótica, veículos autônomos e sistemas automatizados avançam.</div>
    <div class="line">Automatizar tarefas não significa necessariamente eliminar uma profissão inteira.</div>
    <div class="diagram">${S.prof}
  ↓
conjunto de tarefas
  ↓
algumas podem ser automatizadas
  ↓
outras continuam dependendo principalmente de pessoas</div>
    <div class="btnrow"><button class="primary" id="go">Continuar</button></div>`);
  render(n);
  n.querySelector('#go').onclick=screenCrisis;
}

// ---------- 2040 CRISIS ----------
function screenCrisis(){
  const n=el(`${bar(72)}${timelineHTML('2040')}
    <div class="tag">CENÁRIO HIPOTÉTICO, NÃO UMA PREVISÃO</div>
    <div class="line">Empresas de diversos países aceleraram a automação simultaneamente. Milhões de trabalhadores precisam se adaptar a novas funções.</div>
    <div class="line">Seu setor está passando por uma grande transformação.</div>
    <div class="choices" id="c"></div>`);
  const opts=[
    ['Aceitar trabalhar utilizando IA.',{adapt:2,tecnico:1}],
    ['Fazer uma nova formação.',{adapt:2,humano:1}],
    ['Migrar de profissão.',{humano:2}],
    ['Abrir um negócio.',{adapt:2,humano:1}],
    ['Especializar-se.',{tecnico:2,adapt:1}],
    ['Buscar uma função baseada em relações humanas.',{humano:3}],
    ['Trabalhar desenvolvendo ou supervisionando sistemas automatizados.',{tecnico:3}],
    ['Continuar na profissão tradicional.',{tradicional:3}]
  ];
  const c=n.querySelector('#c');
  opts.forEach(([txt,eff])=>{
    const b=document.createElement('div');b.className='choice';b.textContent=txt;
    b.onclick=()=>{Object.entries(eff).forEach(([k,v])=>bump(k,v));log('2040: '+txt);screenConsequence();};
    c.appendChild(b);
  });
  render(n);
}

// ---------- CONSEQUENCE ----------
function computeEnding(){
  const s=S.stats;
  if(s.tradicional>=6 && s.adapt<3) return {cls:'warn',emoji:'🔴',title:'DESEMPREGO TECNOLÓGICO',
    txt:'Sua função sofreu uma automação muito intensa e você está temporariamente procurando uma nova posição. Isso não significa desemprego permanente — significa que uma transição é necessária.'};
  if(s.tradicional>=4) return {cls:'warn',emoji:'🟠',title:'PRESSÃO DA AUTOMAÇÃO',
    txt:'Grande parte das tarefas que você realizava passou a ser automatizada e existem menos vagas tradicionais na sua função original.'};
  if(s.tecnico>=6) return {cls:'',emoji:'🔵',title:'HUMANO + MÁQUINA',
    txt:'Você utiliza IA constantemente e sua produtividade aumentou muito. Seu papel virou o de orientar, revisar e decidir sobre o que as máquinas produzem.'};
  if(s.humano>=6) return {cls:'gold',emoji:'🟡',title:'REQUALIFICAÇÃO',
    txt:'Parte das suas habilidades técnicas perdeu valor de mercado, mas você desenvolveu novas competências ligadas ao julgamento humano e à relação com pessoas.'};
  if(s.adapt>=5 && s.humano>=3) return {cls:'',emoji:'🟣',title:'NOVA PROFISSÃO',
    txt:'As transformações tecnológicas fizeram você migrar para uma ocupação que praticamente não existia quando começou sua carreira.'};
  return {cls:'',emoji:'🟢',title:'PROFISSÃO TRANSFORMADA',
    txt:'Você continua como '+S.prof+', mas suas atividades diárias são muito diferentes das de 2026.'};
}
function screenConsequence(){
  const e=computeEnding();S.ending=e;
  const n=el(`${bar(80)}<div class="eyebrow">SUA TRAJETÓRIA</div>
    <div class="result ${e.cls}"><h3>${e.emoji} ${e.title}</h3><p>${e.txt}</p></div>
    <div class="btnrow"><button class="primary" id="go">Continuar</button></div>`);
  render(n);
  n.querySelector('#go').onclick=screenReveal;
}

// ---------- REVEAL ----------
function screenReveal(){
  const lines=['Mas existe um problema.','Você estava pensando apenas na SUA carreira.',
    '1 pessoa → 1.000 pessoas → 1 milhão → centenas de milhões de trabalhadores',
    'E se essa transformação acontecer simultaneamente em vários países e setores?'];
  let i=0;
  const n=el(`<div id="ln" class="big" style="font-size:24px"></div>
    <div class="btnrow"><button class="primary" id="go" style="display:none">Continuar</button></div>`);
  render(n);
  const ln=n.querySelector('#ln'), go=n.querySelector('#go');
  function step(){ln.textContent=lines[i];i++;if(i<lines.length)setTimeout(step,1900);else go.style.display='inline-block';}
  step();
  go.onclick=screenParadox;
}

// ---------- PARADOX ----------
function screenParadox(){
  const n=el(`${bar(90)}<div class="line">As máquinas poderiam produzir mais bens e serviços utilizando menos trabalho humano.</div>
    <div class="line">Isso seria uma crise… ou uma conquista?</div>
    <div class="scenarios">
      <div class="sc"><b>CENÁRIO A</b><br>Automação aumenta a produtividade, surgem novas profissões e trabalhadores migram para novas atividades.</div>
      <div class="sc"><b>CENÁRIO B</b><br>Automação acontece mais rapidamente do que a criação de novas oportunidades, provocando desemprego tecnológico em grande escala.</div>
      <div class="sc"><b>CENÁRIO C</b><br>A sociedade reorganiza o trabalho. Jornadas diminuem e máquinas realizam grande parte das tarefas repetitivas.</div>
    </div>
    <div class="btnrow"><button class="primary" id="go">Continuar</button></div>`);
  render(n);
  n.querySelector('#go').onclick=screenFinal;
}

// ---------- FINAL ----------
function screenFinal(){
  const lines=['Durante toda essa experiência, você tentou proteger o seu emprego.',
    'Mas talvez essa não seja a pergunta mais importante.',
    'Se máquinas forem capazes de produzir grande parte daquilo que precisamos…',
    '…por que nossa sobrevivência ainda dependeria de trabalhar da mesma maneira?',
    'O problema do futuro talvez não seja simplesmente MÁQUINAS ROUBANDO EMPREGOS.',
    'E sim: COMO A SOCIEDADE VAI SE ADAPTAR QUANDO PRECISAR DE MENOS TRABALHO HUMANO PARA PRODUZIR MAIS?'];
  let i=0;
  const n=el(`<div id="ln" class="big" style="font-size:22px"></div>
    <div class="btnrow"><button class="primary" id="go" style="display:none">Continuar</button></div>`);
  render(n);
  const ln=n.querySelector('#ln'), go=n.querySelector('#go');
  function step(){ln.textContent=lines[i];i++;if(i<lines.length)setTimeout(step,2200);else go.style.display='inline-block';}
  step();
  go.onclick=screenTitle;
}
function screenTitle(){
  const n=el(`<div class="big" style="font-size:26px">O PRIMEIRO DESEMPREGO GLOBAL CAUSADO PELAS MÁQUINAS PODE ACONTECER?</div>
    <div class="line" style="color:var(--dim)">Talvez.<br>Mas a tecnologia, sozinha, não determina o futuro.<br>Educação, economia, empresas, governos e as escolhas da própria sociedade também influenciam o que acontecerá.</div>
    <div class="line" style="margin-top:20px;font-weight:600">Se uma máquina pudesse fazer o seu trabalho amanhã, o que você faria hoje?</div>
    <div class="btnrow"><button class="primary" id="go">Ver minha jornada</button></div>`);
  render(n);
  n.querySelector('#go').onclick=screenSummary;
}

// ---------- SUMMARY ----------
function screenSummary(){
  const e=S.ending;
  let played=[];
  try{played=JSON.parse(localStorage.getItem('esf_endings')||'[]');}catch(err){played=[];}
  played.push(e.title);
  try{localStorage.setItem('esf_endings',JSON.stringify(played));}catch(err){}
  const n=el(`${bar(100)}<div class="eyebrow">SUA JORNADA</div>
    <div class="summary-row"><span>Área</span><span>${S.area}</span></div>
    <div class="summary-row"><span>Profissão</span><span>${S.prof}</span></div>
    <div class="summary-row"><span>Características</span><span>${S.traits.join(', ')||'—'}</span></div>
    <div class="summary-row"><span>Decisões</span><span>${S.choices.length}</span></div>
    <div class="result ${e.cls}"><h3>${e.emoji} ${e.title}</h3><p>${e.txt}</p></div>
    <div class="line" style="color:var(--dim);font-size:13px">Você já jogou ${played.length} vez(es) neste dispositivo.</div>
    <div class="btnrow"><button class="primary" id="restart">RECOMEÇAR MINHA HISTÓRIA</button></div>`);
  render(n);
  n.querySelector('#restart').onclick=()=>{
    S={traits:[],area:null,prof:null,choices:[],stats:{adapt:0,humano:0,tecnico:0,tradicional:0}};
    screenIntro();
  };
}

screenIntro();
</script>
</body>
</html>
