# Aguinaldo
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Aguinaldos</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fredoka:wght@500;600&display=swap">
<style>
:root{--bg:#F6EEF7;--card:#fff;--ink:#2B1B3D;--muted:#6E5C80;--line:#E2D3E8;--a:#C4166B;--on-a:#fff;--focus:#0E8F83;color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#1C1426;--card:#29203A;--ink:#F6EEFB;--muted:#B9A8CC;--line:#41345A;--a:#FF7DB8;--on-a:#1C1426;--focus:#5EDFD2;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#1C1426;--card:#29203A;--ink:#F6EEFB;--muted:#B9A8CC;--line:#41345A;--a:#FF7DB8;--on-a:#1C1426;--focus:#5EDFD2;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*,*::before,*::after{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.4 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;padding-bottom:130px}
main{max-width:560px;margin:0 auto;padding:0 16px}
.flags{height:26px;margin:0 -16px 14px;background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='26'%3E%3Cpath d='M0 0h40L20 26z' fill='%23D6247A'/%3E%3Cpath d='M40 0h40L60 26z' fill='%230E8F83'/%3E%3Cpath d='M80 0h40L100 26z' fill='%23F5B82E'/%3E%3C/svg%3E") repeat-x;box-shadow:inset 0 2px 0 var(--ink)}
h1{margin:0;font:600 2.2rem/1.1 Fredoka,system-ui,sans-serif}
header p{margin:6px 0 0;color:var(--muted)}
#st{display:block;min-height:1.2em;margin:4px 0 12px;font-size:.85rem;color:var(--muted)}
ul{list-style:none;margin:0;padding:0;display:grid;gap:12px}
.row{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:12px;display:grid;gap:12px}
.top{display:flex;gap:8px;align-items:center}
.name{flex:1;min-width:0;background:transparent;color:var(--ink);border:0;border-bottom:1.5px solid var(--line);padding:6px 2px;font:600 1.15rem/1.2 Fredoka,system-ui,sans-serif}
.del{background:none;border:0;color:var(--muted);font:inherit;font-size:.9rem;padding:10px 6px;cursor:pointer}
.line{display:flex;flex-wrap:wrap;align-items:flex-end;gap:12px 16px}
.f{display:grid;gap:4px}
.f small{color:var(--muted);font-size:.8rem}
.box{display:flex;align-items:center;border:1.5px solid var(--line);border-radius:12px;padding:0 10px;height:44px;background:var(--bg)}
.box b{color:var(--muted);font-weight:500;margin-right:4px}
.box input{width:76px;border:0;background:transparent;color:var(--ink);font:inherit;font-size:1.05rem;padding:0;height:100%}
.qty{display:flex;align-items:center;gap:6px}
.qty button{width:44px;height:44px;border-radius:50%;border:1.5px solid var(--a);background:transparent;color:var(--a);font-size:1.4rem;line-height:1;cursor:pointer}
.qty input{width:52px;height:44px;text-align:center;border:1.5px solid var(--line);border-radius:12px;background:var(--bg);color:var(--ink);font:inherit;font-size:1.1rem}
.sub{margin-left:auto;font:600 1.15rem/1 Fredoka,system-ui,sans-serif;padding-bottom:12px}
input[type=number]{-moz-appearance:textfield}
input::-webkit-outer-spin-button,input::-webkit-inner-spin-button{-webkit-appearance:none;margin:0}
:is(button,input):focus-visible{outline:3px solid var(--focus);outline-offset:2px}
.add{width:100%;height:50px;margin-top:14px;border:0;border-radius:14px;background:var(--a);color:var(--on-a);font:600 1.05rem Fredoka,system-ui,sans-serif;cursor:pointer}
#empty{color:var(--muted);text-align:center;padding:24px 0}
.bar{position:fixed;left:0;right:0;bottom:0;background:var(--card);border-top:1px solid var(--line);padding:12px 16px calc(12px + env(safe-area-inset-bottom,0px))}
.bar-in{max-width:560px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:12px}
#count{color:var(--muted);font-size:.9rem}
#total{display:block;font:600 2rem/1.1 Fredoka,system-ui,sans-serif}
.ghost{height:44px;padding:0 16px;border:1.5px solid var(--a);border-radius:12px;background:transparent;color:var(--a);font:600 .95rem Fredoka,system-ui,sans-serif;cursor:pointer}
h2{margin:0;font:600 1.4rem/1.2 Fredoka,system-ui,sans-serif}
[hidden]{display:none!important}
.pay{margin-top:24px;background:var(--card);border:1px solid var(--line);border-radius:16px;padding:16px;display:grid;gap:16px}
.form{display:grid;gap:16px}
fieldset{border:0;padding:0;margin:0;display:grid;gap:8px}
legend{padding:0;margin-bottom:8px;font-weight:600}
.opt{display:flex;align-items:center;gap:12px;min-height:48px;padding:0 14px;border:1.5px solid var(--line);border-radius:12px;cursor:pointer}
.opt:has(input:checked){border-color:var(--a);background:var(--bg)}
.opt input{width:20px;height:20px;margin:0;accent-color:var(--a)}
.opt span{display:flex;justify-content:space-between;flex:1;gap:8px}
.opt small{color:var(--muted)}
dl{margin:0;display:grid;grid-template-columns:1fr auto;gap:6px 12px}
dt{color:var(--muted)}
dd{margin:0;text-align:right}
dt.tot,dd.tot{color:var(--ink);font:600 1.4rem/1.2 Fredoka,system-ui,sans-serif}
#pay{margin-top:0}
#msg{margin:0;min-height:1.2em;color:var(--muted)}
#rcpt{gap:8px;margin:12px 0 16px}
#cont{width:auto;margin:0;padding:0 22px;height:48px}
.wide{width:100%;margin-top:10px}
.txt{width:100%;height:44px;border:1.5px solid var(--line);border-radius:12px;padding:0 12px;background:var(--bg);color:var(--ink);font:inherit;font-size:1.05rem}
h3{margin:0 0 8px;font:600 1.1rem/1.2 Fredoka,system-ui,sans-serif}
.bank{border:1.5px solid var(--line);border-radius:12px;padding:12px;background:var(--bg)}
.bd{grid-template-columns:1fr;gap:2px}
.bd dd{text-align:left;margin-bottom:8px;font-weight:600}
.bd dd:last-child{margin-bottom:0}
.sel{user-select:all;-webkit-user-select:all;word-break:break-all;letter-spacing:.04em}
.note{margin:0 0 12px;color:var(--muted)}
a.add{display:flex;align-items:center;justify-content:center;text-decoration:none}
#sms{margin-top:0}
#again{width:100%;margin-top:10px}
#rbank{margin-bottom:16px}
.back{background:none;border:0;color:var(--a);font:600 1rem Fredoka,system-ui,sans-serif;padding:8px 0;text-align:left;cursor:pointer}
.rl{display:flex;justify-content:space-between;gap:12px}
.rl.sep{border-top:1px solid var(--line);padding-top:8px}
.rl.tot{font:600 1.4rem/1.2 Fredoka,system-ui,sans-serif}
.del{display:none}
.name,.p{pointer-events:none}
.name{border-bottom-color:transparent}
.box{border-color:transparent;background:none;padding:0}
</style>
</head>
<body>
<main>
  <header>
    <div class="flags" aria-hidden="true"></div>
    <h1>Aguinaldos</h1>
    <p>Elige cuántos aguinaldos quieres y continúa para pagar.</p>
    <span id="st" aria-live="polite"></span>
  </header>
  <div id="step1">
  <ul id="list"></ul>
  <p id="empty" hidden>Todavía no hay aguinaldos. Toca “Agregar aguinaldo” para empezar.</p>
  <button class="add" id="add" hidden>Agregar aguinaldo</button>
  <button class="ghost wide" id="clear" hidden>Nuevo pedido</button>
  </div>
  <section class="pay" id="step2" aria-labelledby="pay-h" hidden>
    <button class="back" id="back">← Volver a los aguinaldos</button>
    <h2 id="pay-h">Entrega y pago</h2>
    <div class="form" id="pay-form">
      <fieldset>
        <legend>Entrega</legend>
        <label class="opt"><input type="radio" name="del" value="punto"><span>Punto medio <small>Gratis</small></span></label>
        <label class="opt"><input type="radio" name="del" value="domicilio"><span>A domicilio <small id="fee-t"></small></span></label>
      </fieldset>
      <fieldset id="spots"><legend>Punto medio de entrega</legend></fieldset>
      <div id="dom" class="form">
        <label class="f" hidden><small>Costo del envío a domicilio</small><span class="box"><b>$</b><input id="fee" type="number" inputmode="decimal" min="0" step="0.5"></span></label>
        <label class="f"><small>Dirección o referencias</small><input id="addr" class="txt" placeholder="Calle, número, colonia"></label>
      </div>
      <fieldset>
        <legend>Forma de pago</legend>
        <label class="opt"><input type="radio" name="pay" value="efectivo"><span>Efectivo</span></label>
        <label class="opt"><input type="radio" name="pay" value="transferencia"><span>Transferencia</span></label>
      </fieldset>
      <div id="bank" class="bank" hidden>
        <h3>Datos para la transferencia</h3>
        <dl class="bd"><dt>CLABE interbancaria</dt><dd class="sel">638180000192990462</dd><dt>Nombre de la cuenta</dt><dd>Hans Morales Hernández</dd><dt>Banco</dt><dd>NuBank</dd></dl>
      </div>
      <dl>
        <dt>Aguinaldos</dt><dd id="s-sub"></dd>
        <dt>Envío</dt><dd id="s-ship"></dd>
        <dt class="tot">Total</dt><dd class="tot" id="s-tot"></dd>
      </dl>
      <button class="add" id="pay">Pagar</button>
      <p id="msg" aria-live="polite"></p>
    </div>
    <div id="done" hidden>
      <h2>Pedido pagado</h2>
      <ul id="rcpt"></ul>
      <div id="rbank"></div>
      <p class="note">Toca el botón y envía el mensaje para avisar dónde se entrega.</p>
      <a class="add" id="sms" href="#" target="_blank" rel="noopener">Avisar por WhatsApp</a>
      <button class="ghost" id="again">Empezar otro pedido</button>
    </div>
  </section>
</main>
<footer class="bar">
  <div class="bar-in">
    <div><span id="count">0 aguinaldos</span><strong id="total">$0.00</strong></div>
    <button class="add" id="cont">Continuar</button>
  </div>
</footer>
<script>
(function(){
var KEY='aguinaldos-v1';
var fmt=new Intl.NumberFormat('es-MX',{style:'currency',currency:'MXN'});
var $=function(s){return document.querySelector(s)};
var uid=function(){return Math.random().toString(36).slice(2,9)};
var num=function(v){var x=parseFloat(v);return isFinite(x)&&x>=0?x:0};
var list=$('#list'),st=$('#st');
var touched=false,dbRef=null,timer=null;

function clean(items){return items.map(function(i){return{id:String(i.id||uid()),name:String(i.name||''),price:num(i.price),qty:Math.floor(num(i.qty))}})}
function norm(s){return{items:clean(s.items),fee:s.fee==null?25:num(s.fee),delivery:s.delivery==='domicilio'?'domicilio':'punto',pay:s.pay==='transferencia'?'transferencia':'efectivo'}}
function readLocal(){return null}
function writeLocal(){}

var state=readLocal()||{items:[['Aguinaldo',60]].map(function(p){return{id:uid(),name:p[0],price:p[1],qty:0}}),fee:10,delivery:'punto',pay:'efectivo'};

function save(){}

function totals(){
  var t=0,c=0;
  state.items.forEach(function(i){t+=i.price*i.qty;c+=i.qty});
  var ship=(state.delivery==='domicilio'&&c>0)?state.fee:0;
  $('#total').textContent=fmt.format(t+($('#step2').hidden?0:ship));
  $('#s-sub').textContent=fmt.format(t);
  $('#s-ship').textContent=state.delivery==='domicilio'?(c>0?fmt.format(state.fee):'—'):'Gratis';
  $('#s-tot').textContent=fmt.format(t+ship);
  $('#fee-t').textContent=fmt.format(state.fee);
  $('#count').textContent=c+(c===1?' aguinaldo':' aguinaldos');
  list.querySelectorAll('.row').forEach(function(r){
    var i=state.items.find(function(x){return x.id===r.dataset.id});
    if(i)r.querySelector('.sub').textContent=fmt.format(i.price*i.qty);
  });
}

function twoTap(btn,label,ask,fn){
  var t;
  btn.onclick=function(){
    if(btn.dataset.ask){clearTimeout(t);delete btn.dataset.ask;btn.textContent=label;fn();return}
    btn.dataset.ask=1;btn.textContent=ask;
    t=setTimeout(function(){delete btn.dataset.ask;btn.textContent=label},3000);
  };
}

function row(it){
  var li=document.createElement('li');li.className='row';li.dataset.id=it.id;
  li.innerHTML='<div class="top"><input class="name" placeholder="Nombre del aguinaldo" aria-label="Nombre del aguinaldo"><button class="del">Quitar</button></div>'+
  '<div class="line">'+
  '<label class="f"><small>Precio c/u</small><span class="box"><b>$</b><input class="p" type="number" inputmode="decimal" min="0" step="0.5"></span></label>'+
  '<div class="f"><small>Cantidad</small><div class="qty"><button class="m" aria-label="Menos">−</button><input class="q" type="number" inputmode="numeric" min="0" step="1" aria-label="Cantidad"><button class="a" aria-label="Más">+</button></div></div>'+
  '<output class="sub"></output></div>';
  var n=li.querySelector('.name'),p=li.querySelector('.p'),q=li.querySelector('.q');
  n.value=it.name;p.value=it.price;q.value=it.qty;n.readOnly=true;p.readOnly=true;
  [p,q].forEach(function(el){el.onfocus=function(){el.select()}});
  n.oninput=function(){it.name=n.value;save()};
  p.oninput=function(){it.price=num(p.value);totals();save()};
  q.oninput=function(){it.qty=Math.floor(num(q.value));totals();save()};
  li.querySelector('.m').onclick=function(){it.qty=Math.max(0,it.qty-1);q.value=it.qty;totals();save()};
  li.querySelector('.a').onclick=function(){it.qty+=1;q.value=it.qty;totals();save()};
  twoTap(li.querySelector('.del'),'Quitar','¿Seguro?',function(){
    state.items=state.items.filter(function(x){return x.id!==it.id});save();render();
  });
  return li;
}

function render(){
  list.textContent='';
  state.items.forEach(function(it){list.append(row(it))});
  $('#empty').hidden=state.items.length>0;sync();
  totals();
}

$('#add').onclick=function(){
  state.items.push({id:uid(),name:'',price:0,qty:0});
  save();render();
  list.lastElementChild.querySelector('.name').focus();
};
twoTap($('#clear'),'Nuevo pedido','¿Borrar pedido?',function(){
  state.items.forEach(function(i){i.qty=0});save();render();resetOrder();$('#done').hidden=true;$('#pay-form').hidden=false;
});

function go(n){
  $('#step1').hidden=n!==1;$('#step2').hidden=n!==2;$('#cont').hidden=n!==1;
  $('#done').hidden=true;$('#pay-form').hidden=false;
  st.textContent='';totals();
  window.scrollTo({top:0,behavior:'smooth'});
}
function sync(){
  document.querySelectorAll('input[name=del]').forEach(function(r){r.checked=r.value===state.delivery});
  document.querySelectorAll('input[name=pay]').forEach(function(r){r.checked=r.value===state.pay});
  $('#fee').value=state.fee;vis();
}
document.querySelectorAll('input[name=del]').forEach(function(r){r.onchange=function(){state.delivery=r.value;vis();totals();save()}});
document.querySelectorAll('input[name=pay]').forEach(function(r){r.onchange=function(){state.pay=r.value;vis();save()}});
$('#fee').oninput=function(){state.fee=num(this.value);totals();save()};
$('#fee').onfocus=function(){this.select()};
$('#cont').onclick=function(){
  if(!state.items.some(function(i){return i.qty>0})){st.textContent='Agrega al menos un aguinaldo para continuar.';return}
  go(2);
};
$('#back').onclick=function(){go(1)};

var spot='',addr='';
var SPOTS=['Cruz Blanca','Centro','El Deportivo','Entrada Los Amores','Centro San Javier','Crucero de San Javier'];
SPOTS.forEach(function(s){
  var l=document.createElement('label');l.className='opt';
  var i=document.createElement('input');i.type='radio';i.name='spot';i.value=s;
  i.onchange=function(){spot=s;$('#msg').textContent=''};
  l.append(i,mk('span',s));$('#spots').append(l);
});
$('#addr').oninput=function(){addr=this.value;$('#msg').textContent=''};
function vis(){$('#spots').hidden=state.delivery!=='punto';$('#dom').hidden=state.delivery!=='domicilio';$('#bank').hidden=state.pay!=='transferencia'}
function resetOrder(){spot='';addr='';$('#addr').value='';document.querySelectorAll('input[name=spot]').forEach(function(r){r.checked=false})}
function mk(tag,text){var e=document.createElement(tag);e.textContent=text;return e}
function rl(a,b,cls){var li=document.createElement('li');li.className='rl'+(cls?' '+cls:'');li.append(mk('span',a),mk('b',b));return li}
$('#pay').onclick=function(){
  var its=state.items.filter(function(i){return i.qty>0});
  if(!its.length){$('#msg').textContent='Agrega al menos un aguinaldo para pagar.';return}
  $('#msg').textContent='';
  if(state.delivery==='punto'&&!spot){$('#msg').textContent='Elige el punto medio de entrega.';return}
  if(state.delivery==='domicilio'&&!addr.trim()){$('#msg').textContent='Escribe la dirección de entrega.';return}
  var t=0;its.forEach(function(i){t+=i.price*i.qty});
  var dom=state.delivery==='domicilio',ship=dom?state.fee:0;
  var r=$('#rcpt');r.textContent='';
  its.forEach(function(i){r.append(rl(i.qty+' × '+(i.name||'Aguinaldo'),fmt.format(i.price*i.qty)))});
  r.append(rl('Entrega',dom?'A domicilio':'Punto medio','sep'));
  r.append(rl('Lugar',dom?addr.trim():spot));
  r.append(rl('Envío',dom?fmt.format(ship):'Gratis'));
  r.append(rl('Pago',state.pay==='efectivo'?'Efectivo':'Transferencia'));
  r.append(rl('Total',fmt.format(t+ship),'tot'));
  var lines=['Pedido de aguinaldos'];
  its.forEach(function(i){lines.push(i.qty+' × '+(i.name||'Aguinaldo')+' - '+fmt.format(i.price*i.qty))});
  lines.push('Entrega: '+(dom?'A domicilio, '+addr.trim():'Punto medio, '+spot));
  lines.push('Pago: '+(state.pay==='efectivo'?'Efectivo':'Transferencia'));
  lines.push('Total: '+fmt.format(t+ship));
  $('#sms').href='https://wa.me/527717093615?text='+encodeURIComponent(lines.join('\n'));
  var rb=$('#rbank');rb.textContent='';
  if(state.pay==='transferencia'){var bc=$('#bank').cloneNode(true);bc.removeAttribute('id');bc.hidden=false;rb.append(bc)}
  $('#pay-form').hidden=true;$('#done').hidden=false;
  $('#done').scrollIntoView({behavior:'smooth',block:'start'});
};
$('#again').onclick=function(){
  state.items.forEach(function(i){i.qty=0});save();render();
  resetOrder();
  $('#done').hidden=true;$('#pay-form').hidden=false;
  go(1);
};

render();

})();
</script>
</body>
</html>
