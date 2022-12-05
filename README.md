# projetil-calculadora-de-trajeto
Projétil: Calculadora de Trajetória - opencode/html
<html><head><title>Projétil: Calculadora de Trajetória</title>

<meta http-equiv="content-type" content="text/html; charset=UTF-8">
<link rel="icon" type="image/png" href="../../../imagens/favicon.ico">
<meta name="description" content="O portal Ficou Mais Fácil foi eleborado baseado em um moderno conceito de educação que permite a continuidade do aprendizado em casa, através de atividades, vídeos, textos, dicas e muito mais. Com linguagem direta e descomplicada, o estudante terá sempre acesso a um espaço interativo e dinâmico onde poderá aprofundar seus conhecimentos de forma rápida e eficiente.">
<meta name="copyright" content="Ficou Mais Fácil">
<script src="https://apis.google.com/_/scs/abc-static/_/js/k=gapi.lb.pt_BR.6bdaKiuQqKA.O/m=gapi_iframes_style_bubble/exm=auth,ytsubscribe/rt=j/sv=1/d=1/ed=1/rs=AHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw/cb=gapi.loaded_2?le=scs" async=""></script><script src="https://apis.google.com/_/scs/abc-static/_/js/k=gapi.lb.pt_BR.6bdaKiuQqKA.O/m=auth/exm=ytsubscribe/rt=j/sv=1/d=1/ed=1/rs=AHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw/cb=gapi.loaded_1?le=scs" async=""></script><script src="https://apis.google.com/_/scs/abc-static/_/js/k=gapi.lb.pt_BR.6bdaKiuQqKA.O/m=ytsubscribe/rt=j/sv=1/d=1/ed=1/rs=AHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw/cb=gapi.loaded_0?le=scs" async=""></script><script src="https://connect.facebook.net/pt_BR/sdk.js?hash=aaed40aeff688e7aa45df2fd21c7fe1e" async="" crossorigin="anonymous"></script><script id="facebook-jssdk" src="//connect.facebook.net/pt_BR/sdk.js"></script><script async="" src="//www.google-analytics.com/analytics.js"></script><script language="JavaScript">
function calculate()
{
document.calc.range.value = "não pode resolver";
document.calc.height.value = "";
document.calc.time.value = "";
document.calc.speed.value = "";
var Vo = parseFloat(document.calc.Vel_o.value);
var th = parseFloat(document.calc.Theta.value); var Yo = parseFloat(document.calc.Hgt_o.value);
if ((th > 90.0)||(th < 0.0)||(Vo < 0.0)) return;
th = (Math.PI/180.0)*th;
var Ge = parseFloat(9.81);
var Vx = Vo*Math.cos(th); var Vy = Vo*Math.sin(th); var hgt = Yo + Vy*Vy/(2*Ge); if (hgt < 0.0) return;
var upt = Vy/Ge; var dnt = Math.sqrt(2*hgt/Ge); var rng = Vx*(upt + dnt); var imp = upt + dnt;
var spd = Math.sqrt((Ge*dnt)*(Ge*dnt) + Vx*Vx);
if(document.calc.group1[0].checked) {
document.calc.range.value = Math.round(100000.0*rng)/100000.0;
document.calc.height.value = Math.round(100000.0*hgt)/100000.0;
document.calc.time.value = Math.round(100000.0*imp)/100000.0;
document.calc.speed.value = Math.round(100000.0*spd)/100000.0;
}
else
{
document.calc.range.value = rng;
document.calc.height.value = hgt;
document.calc.time.value = imp;
document.calc.speed.value = spd;
}
}
function allclear()
{
document.calc.range.value = '0';
document.calc.height.value = '0';
document.calc.time.value = '0';
document.calc.speed.value = '0';
}
</script>
<style>.gc-bubbleDefault{background-color:transparent!important;text-align:left;padding:0!important;margin:0!important;border:0!important;table-layout:auto!important}.gc-reset{background-color:transparent!important;border:0!important;padding:0!important;margin:0!important;text-align:left}.pls-bubbleTop{border-bottom:1px solid #ccc!important}.pls-contentLeft,.pls-topTail,.pls-vertShimLeft{background-image:url(//ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/border_3.gif)!important}.pls-topTail{background-repeat:repeat-x!important;background-position:bottom!important}.pls-vertShim{background-color:#fff!important;text-align:right}.tbl-grey .pls-vertShim{background-color:#f5f5f5!important}.pls-vertShimLeft{background-repeat:repeat-y!important;background-position:100%!important;height:4px}.pls-vertShimRight{height:4px}.pls-confirm-container .pls-vertShim{background-color:#fff3c2!important}.pls-contentWrap{background-color:#fff!important;position:relative!important;vertical-align:top}.pls-contentLeft{background-repeat:repeat-y;background-position:100%;vertical-align:top}.pls-dropRight{background-image:url(//ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/bubbleDropR_3.png)!important;background-repeat:repeat-y!important;vertical-align:top}.pls-dropBL,.pls-dropTR .pls-dropBR,.pls-tailleft,.pls-vert,.pls-vert img{vertical-align:top}.pls-dropBottom{background-image:url(//ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/bubbleDropB_3.png)!important;background-repeat:repeat-x!important;width:100%;vertical-align:top}.pls-topLeft{background:inherit!important;text-align:right;vertical-align:bottom}.pls-topRight{background:inherit!important;text-align:left;vertical-align:bottom}.pls-bottomLeft{background:inherit!important;text-align:right}.pls-bottomRight{background:inherit!important;text-align:left;vertical-align:top}.pls-tailbottom,.pls-tailleft,.pls-tailright,.pls-tailtop{display:none;position:relative}.pls-dropBL,.pls-dropBR,.pls-dropTR,.pls-tailbottom,.pls-tailleft,.pls-tailright,.pls-tailtop{background-image:url(//ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/bubbleSprite_3.png)!important;background-repeat:no-repeat}.tbl-grey .pls-dropBL,.tbl-grey .pls-dropBR,.tbl-grey .pls-dropTR,.tbl-grey .pls-tailbottom,.tbl-grey .pls-tailleft,.tbl-grey .pls-tailright,.tbl-grey .pls-tailtop{background-image:url(//ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/bubbleSprite-grey.png)!important}.pls-tailbottom{background-position:-23px 0}.pls-confirm-container .pls-tailbottom{background-position:-23px -10px}.pls-tailtop{background-position:-19px -20px}.pls-tailright{background-position:0 0}.pls-tailleft{background-position:-10px 0}.pls-tailtop{vertical-align:top}.gc-bubbleDefault td{line-height:0;font-size:0}.pls-tailbottom,.pls-topLeft img,.pls-topRight img{vertical-align:bottom}.bubbleDropTR,.pls-bottomLeft,.pls-bottomLeft img,.pls-dropBottom img,.pls-dropBottomL img,.pls-dropBottomR img{vertical-align:top}.pls-dropTR{background-position:0 -22px}.pls-dropBR{background-position:0 -27px}.pls-dropBL{background-position:0 -16px}.pls-spacerbottom,.pls-spacerleft,.pls-spacerright,.pls-spacertop{position:static!important}.pls-spinner{bottom:0;position:absolute;left:0;margin:auto;right:0;top:0}</style><style type="text/css" data-fbcssmodules="css:fb.css.base css:fb.css.dialog css:fb.css.iframewidget css:fb.css.customer_chat_plugin_iframe">.fb_hidden{position:absolute;top:-10000px;z-index:10001}.fb_reposition{overflow:hidden;position:relative}.fb_invisible{display:none}.fb_reset{background:none;border:0;border-spacing:0;color:#000;cursor:auto;direction:ltr;font-family:'lucida grande', tahoma, verdana, arial, sans-serif;font-size:11px;font-style:normal;font-variant:normal;font-weight:normal;letter-spacing:normal;line-height:1;margin:0;overflow:visible;padding:0;text-align:left;text-decoration:none;text-indent:0;text-shadow:none;text-transform:none;visibility:visible;white-space:normal;word-spacing:normal}.fb_reset>div{overflow:hidden}@keyframes fb_transform{from{opacity:0;transform:scale(.95)}to{opacity:1;transform:scale(1)}}.fb_animate{animation:fb_transform .3s forwards}
.fb_hidden{position:absolute;top:-10000px;z-index:10001}.fb_reposition{overflow:hidden;position:relative}.fb_invisible{display:none}.fb_reset{background:none;border:0;border-spacing:0;color:#000;cursor:auto;direction:ltr;font-family:'lucida grande', tahoma, verdana, arial, sans-serif;font-size:11px;font-style:normal;font-variant:normal;font-weight:normal;letter-spacing:normal;line-height:1;margin:0;overflow:visible;padding:0;text-align:left;text-decoration:none;text-indent:0;text-shadow:none;text-transform:none;visibility:visible;white-space:normal;word-spacing:normal}.fb_reset>div{overflow:hidden}@keyframes fb_transform{from{opacity:0;transform:scale(.95)}to{opacity:1;transform:scale(1)}}.fb_animate{animation:fb_transform .3s forwards}
.fb_dialog{background:rgba(82, 82, 82, .7);position:absolute;top:-10000px;z-index:10001}.fb_dialog_advanced{border-radius:8px;padding:10px}.fb_dialog_content{background:#fff;color:#373737}.fb_dialog_close_icon{background:url(https://connect.facebook.net/rsrc.php/v3/yq/r/IE9JII6Z1Ys.png) no-repeat scroll 0 0 transparent;cursor:pointer;display:block;height:15px;position:absolute;right:18px;top:17px;width:15px}.fb_dialog_mobile .fb_dialog_close_icon{left:5px;right:auto;top:5px}.fb_dialog_padding{background-color:transparent;position:absolute;width:1px;z-index:-1}.fb_dialog_close_icon:hover{background:url(https://connect.facebook.net/rsrc.php/v3/yq/r/IE9JII6Z1Ys.png) no-repeat scroll 0 -15px transparent}.fb_dialog_close_icon:active{background:url(https://connect.facebook.net/rsrc.php/v3/yq/r/IE9JII6Z1Ys.png) no-repeat scroll 0 -30px transparent}.fb_dialog_iframe{line-height:0}.fb_dialog_content .dialog_title{background:#6d84b4;border:1px solid #365899;color:#fff;font-size:14px;font-weight:bold;margin:0}.fb_dialog_content .dialog_title>span{background:url(https://connect.facebook.net/rsrc.php/v3/yd/r/Cou7n-nqK52.gif) no-repeat 5px 50%;float:left;padding:5px 0 7px 26px}body.fb_hidden{height:100%;left:0;margin:0;overflow:visible;position:absolute;top:-10000px;transform:none;width:100%}.fb_dialog.fb_dialog_mobile.loading{background:url(https://connect.facebook.net/rsrc.php/v3/ya/r/3rhSv5V8j3o.gif) white no-repeat 50% 50%;min-height:100%;min-width:100%;overflow:hidden;position:absolute;top:0;z-index:10001}.fb_dialog.fb_dialog_mobile.loading.centered{background:none;height:auto;min-height:initial;min-width:initial;width:auto}.fb_dialog.fb_dialog_mobile.loading.centered #fb_dialog_loader_spinner{width:100%}.fb_dialog.fb_dialog_mobile.loading.centered .fb_dialog_content{background:none}.loading.centered #fb_dialog_loader_close{clear:both;color:#fff;display:block;font-size:18px;padding-top:20px}#fb-root #fb_dialog_ipad_overlay{background:rgba(0, 0, 0, .4);bottom:0;left:0;min-height:100%;position:absolute;right:0;top:0;width:100%;z-index:10000}#fb-root #fb_dialog_ipad_overlay.hidden{display:none}.fb_dialog.fb_dialog_mobile.loading iframe{visibility:hidden}.fb_dialog_mobile .fb_dialog_iframe{position:sticky;top:0}.fb_dialog_content .dialog_header{background:linear-gradient(from(#738aba), to(#2c4987));border-bottom:1px solid;border-color:#043b87;box-shadow:white 0 1px 1px -1px inset;color:#fff;font:bold 14px Helvetica, sans-serif;text-overflow:ellipsis;text-shadow:rgba(0, 30, 84, .296875) 0 -1px 0;vertical-align:middle;white-space:nowrap}.fb_dialog_content .dialog_header table{height:43px;width:100%}.fb_dialog_content .dialog_header td.header_left{font-size:12px;padding-left:5px;vertical-align:middle;width:60px}.fb_dialog_content .dialog_header td.header_right{font-size:12px;padding-right:5px;vertical-align:middle;width:60px}.fb_dialog_content .touchable_button{background:linear-gradient(from(#4267B2), to(#2a4887));background-clip:padding-box;border:1px solid #29487d;border-radius:3px;display:inline-block;line-height:18px;margin-top:3px;max-width:85px;padding:4px 12px;position:relative}.fb_dialog_content .dialog_header .touchable_button input{background:none;border:none;color:#fff;font:bold 12px Helvetica, sans-serif;margin:2px -12px;padding:2px 6px 3px 6px;text-shadow:rgba(0, 30, 84, .296875) 0 -1px 0}.fb_dialog_content .dialog_header .header_center{color:#fff;font-size:16px;font-weight:bold;line-height:18px;text-align:center;vertical-align:middle}.fb_dialog_content .dialog_content{background:url(https://connect.facebook.net/rsrc.php/v3/y9/r/jKEcVPZFk-2.gif) no-repeat 50% 50%;border:1px solid #4a4a4a;border-bottom:0;border-top:0;height:150px}.fb_dialog_content .dialog_footer{background:#f5f6f7;border:1px solid #4a4a4a;border-top-color:#ccc;height:40px}#fb_dialog_loader_close{float:left}.fb_dialog.fb_dialog_mobile .fb_dialog_close_icon{visibility:hidden}#fb_dialog_loader_spinner{animation:rotateSpinner 1.2s linear infinite;background-color:transparent;background-image:url(https://connect.facebook.net/rsrc.php/v3/yD/r/t-wz8gw1xG1.png);background-position:50% 50%;background-repeat:no-repeat;height:24px;width:24px}@keyframes rotateSpinner{0%{transform:rotate(0deg)}100%{transform:rotate(360deg)}}
.fb_iframe_widget{display:inline-block;position:relative}.fb_iframe_widget span{display:inline-block;position:relative;text-align:justify}.fb_iframe_widget iframe{position:absolute}.fb_iframe_widget_fluid_desktop,.fb_iframe_widget_fluid_desktop span,.fb_iframe_widget_fluid_desktop iframe{max-width:100%}.fb_iframe_widget_fluid_desktop iframe{min-width:220px;position:relative}.fb_iframe_widget_lift{z-index:1}.fb_iframe_widget_fluid{display:inline}.fb_iframe_widget_fluid span{width:100%}
.fb_mpn_mobile_landing_page_slide_out{animation-duration:200ms;animation-name:fb_mpn_landing_page_slide_out;transition-timing-function:ease-in}.fb_mpn_mobile_landing_page_slide_out_from_left{animation-duration:200ms;animation-name:fb_mpn_landing_page_slide_out_from_left;transition-timing-function:ease-in}.fb_mpn_mobile_landing_page_slide_up{animation-duration:500ms;animation-name:fb_mpn_landing_page_slide_up;transition-timing-function:ease-in}.fb_mpn_mobile_bounce_in{animation-duration:300ms;animation-name:fb_mpn_bounce_in;transition-timing-function:ease-in}.fb_mpn_mobile_bounce_out{animation-duration:300ms;animation-name:fb_mpn_bounce_out;transition-timing-function:ease-in}.fb_mpn_mobile_bounce_out_v2{animation-duration:300ms;animation-name:fb_mpn_fade_out;transition-timing-function:ease-in}.fb_customer_chat_bounce_in_v2{animation-duration:300ms;animation-name:fb_bounce_in_v2;transition-timing-function:ease-in}.fb_customer_chat_bounce_in_from_left{animation-duration:300ms;animation-name:fb_bounce_in_from_left;transition-timing-function:ease-in}.fb_customer_chat_bounce_out_v2{animation-duration:300ms;animation-name:fb_bounce_out_v2;transition-timing-function:ease-in}.fb_customer_chat_bounce_out_from_left{animation-duration:300ms;animation-name:fb_bounce_out_from_left;transition-timing-function:ease-in}.fb_invisible_flow{display:inherit;height:0;overflow-x:hidden;width:0}@keyframes fb_mpn_landing_page_slide_out{0%{margin:0 12px;width:100% - 24px}60%{border-radius:18px}100%{border-radius:50%;margin:0 24px;width:60px}}@keyframes fb_mpn_landing_page_slide_out_from_left{0%{left:12px;width:100% - 24px}60%{border-radius:18px}100%{border-radius:50%;left:12px;width:60px}}@keyframes fb_mpn_landing_page_slide_up{0%{bottom:0;opacity:0}100%{bottom:24px;opacity:1}}@keyframes fb_mpn_bounce_in{0%{opacity:.5;top:100%}100%{opacity:1;top:0}}@keyframes fb_mpn_fade_out{0%{bottom:30px;opacity:1}100%{bottom:0;opacity:0}}@keyframes fb_mpn_bounce_out{0%{opacity:1;top:0}100%{opacity:.5;top:100%}}@keyframes fb_bounce_in_v2{0%{opacity:0;transform:scale(0, 0);transform-origin:bottom right}50%{transform:scale(1.03, 1.03);transform-origin:bottom right}100%{opacity:1;transform:scale(1, 1);transform-origin:bottom right}}@keyframes fb_bounce_in_from_left{0%{opacity:0;transform:scale(0, 0);transform-origin:bottom left}50%{transform:scale(1.03, 1.03);transform-origin:bottom left}100%{opacity:1;transform:scale(1, 1);transform-origin:bottom left}}@keyframes fb_bounce_out_v2{0%{opacity:1;transform:scale(1, 1);transform-origin:bottom right}100%{opacity:0;transform:scale(0, 0);transform-origin:bottom right}}@keyframes fb_bounce_out_from_left{0%{opacity:1;transform:scale(1, 1);transform-origin:bottom left}100%{opacity:0;transform:scale(0, 0);transform-origin:bottom left}}@keyframes slideInFromBottom{0%{opacity:.1;transform:translateY(100%)}100%{opacity:1;transform:translateY(0)}}@keyframes slideInFromBottomDelay{0%{opacity:0;transform:translateY(100%)}97%{opacity:0;transform:translateY(100%)}100%{opacity:1;transform:translateY(0)}}</style></head>
<body style="color: black; background-color: white;">
<div style="text-align: center;"><a href="../../../apoio.php"><img title="Material de Apoio" alt="Material de Apoio" src="../../../imagens/headinglivros.jpg"></a></div>
<script async="" src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<script>
(adsbygoogle = window.adsbygoogle || []).push({
google_ad_client: "ca-pub-5900989438283878",
enable_page_level_ads: true
});
</script>
<script>
(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
})(window,document,'script','//www.google-analytics.com/analytics.js','ga');
ga('create', 'UA-68422435-1', 'auto');
ga('send', 'pageview');
</script>
<script async="" src="//pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script><!-- DoSiteFMF --><ins class="adsbygoogle" style="display: block;" data-ad-client="ca-pub-5900989438283878" data-ad-slot="7276821741" data-ad-format="auto"><iframe id="aswift_0" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;"><iframe id="google_ads_frame0"></iframe></iframe></ins>
<script>
(adsbygoogle = window.adsbygoogle || []).push({});
</script>
<center>
<h1><font color="green"><b>Projétil:
Calculadora de Trajetória</b></font></h1>
</center>
<center><img src="traj.gif">
<form name="calc"><br>
<table>
<tbody>
<tr>
<td></td>
<td><b>Entre com os valores:</b></td>
<td></td>
</tr>
<tr>
<td><tt>V<sub>o</sub></tt> </td>
<td>= <input maxlength="30" value="0" name="Vel_o"> </td>
<td>metros/segundos
</td>
</tr>
<tr>
<td><tt>θº</tt> </td>
<td>= <input maxlength="30" value="0" name="Theta"> </td>
<td>graus
</td>
</tr>
<tr>
<td><tt>Y<sub>o</sub></tt> </td>
<td>= <input maxlength="30" value="0" name="Hgt_o"> </td>
<td>metros
</td>
</tr>
<tr>
<td></td>
<td><b>Resultados:</b></td>
<td></td>
</tr>
<tr>
<td><tt>R</tt> </td>
<td>= <input maxlength="30" value="0" name="range" readonly="readonly"> </td>
<td>metros
</td>
</tr>
<tr>
<td><tt>H</tt> </td>
<td>= <input maxlength="30" value="0" name="height" readonly="readonly"> </td>
<td>metros
</td>
</tr>
<tr>
<td><tt>T</tt> </td>
<td>= <input maxlength="30" value="0" name="time" readonly="readonly"> </td>
<td>segundos
</td>
</tr>
<tr>
<td><tt>V<sub>f</sub></tt> </td>
<td>= <input maxlength="30" value="0" name="speed" readonly="readonly"> </td>
<td>metros/segundos
</td>
</tr>
</tbody>
</table>
<p><input checked="checked" value="rnd" name="group1" type="radio">
Arredondar&nbsp;&nbsp; <input value="nor" name="group1" type="radio"> Sem arredondar </p>
<p><input onclick="calculate()" value="Calcular" type="button"> <input onclick="allclear()" value="Limpar" type="button"> </p>
</form>
</center>
<p align="justify">Calcule a altura máxima, intervalo,
tempo no ar e velocidade de impacto de um projétil balístico . Os
cálculos usam a aceleração aproximada da gravidade sobre a superfície
da terra (9,81 m/s<sup>2</sup>) sem considerar a
resistência do ar. Insira a velocidade inicial, o ângulo inicial e a
altura em relação à superfície do projétil; selecionando a opção de
arredondamento desejado e em seguida, pressione o botão <b>Calcular</b>.
Todas as entradas são zeradas pressionando o botão <b>Limpar</b>.
Se o programa retornar a mensagem de erro: <b>não pode resolver</b>,
então: o ângulo inicial estáora do intervalo 0 . . . 90º, ou a
velocidade é negativa, ou há um valor negativo para a <tt>y<sub>o</sub></tt>
(<i>altura inicial</i>) resulta em um valor negativo de H (<i>altura
máxima</i>).
</p>
<br>
<h3>
<p align="justify">Este portal está em constante
atualização, portanto, siga-nos
no <a href="http://www.facebook.com/ficoumaisfacil">Facebook</a>
e inscreva-se no nosso canal no <a href="https://www.youtube.com/channel/UCJ7IWmUQ5VgqPhS6K9lnvWw">Youtube</a>
(links abaixo),
para ser notificado sempre que fizermos novas postagens. Fique em dia
com os novos vídeos e conteúdos.</p>
</h3>
<hr>
<script>
window.fbAsyncInit = function() {
FB.init({
appId : '419052808285249',
xfbml : true,
version : 'v2.5'
});
};
(function(d, s, id){
var js, fjs = d.getElementsByTagName(s)[0];
if (d.getElementById(id)) {return;}
js = d.createElement(s); js.id = id;
js.src = "//connect.facebook.net/pt_BR/sdk.js";
fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));
</script>
<center>
<script src="https://apis.google.com/js/platform.js" gapi_processed="true"></script>
<script>
function onYtEvent(payload) {
if (payload.eventType == 'subscribe') {
// Add code to handle subscribe event.
} else if (payload.eventType == 'unsubscribe') {
// Add code to handle unsubscribe event.
}
if (window.console) { // for debugging only
window.console.log('YT event: ', payload);
}
}
</script>&nbsp;&nbsp;
<div id="___ytsubscribe_0" style="text-indent: 0px; margin: 0px; padding: 0px; background: transparent; border-style: none; float: none; line-height: normal; font-size: 1px; vertical-align: baseline; display: inline-block; width: 121px; height: 24px;"><iframe ng-non-bindable="" frameborder="0" hspace="0" marginheight="0" marginwidth="0" scrolling="no" style="position: static; top: 0px; width: 121px; margin: 0px; border-style: none; left: 0px; visibility: visible; height: 24px;" tabindex="0" vspace="0" width="100%" id="I0_1670280633596" name="I0_1670280633596" src="https://www.youtube.com/subscribe_embed?usegapi=1&amp;channelid=UCJ7IWmUQ5VgqPhS6K9lnvWw&amp;layout=default&amp;count=default&amp;origin=https%3A%2F%2Fwww.ficoumaisfacil.com.br&amp;gsrc=3p&amp;ic=1&amp;jsh=m%3B%2F_%2Fscs%2Fabc-static%2F_%2Fjs%2Fk%3Dgapi.lb.pt_BR.6bdaKiuQqKA.O%2Fd%3D1%2Frs%3DAHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw%2Fm%3D__features__#_methods=onPlusOne%2C_ready%2C_close%2C_open%2C_resizeMe%2C_renderstart%2Concircled%2Cdrefresh%2Cerefresh%2Conytevent%2Conload&amp;id=I0_1670280633596&amp;_gfid=I0_1670280633596&amp;parent=https%3A%2F%2Fwww.ficoumaisfacil.com.br&amp;pfname=&amp;rpctoken=17821323" data-gapiattached="true"></iframe></div>
&nbsp;
<div class="fb-like fb_iframe_widget" data-share="true" data-width="450" data-show-faces="true" fb-xfbml-state="rendered" fb-iframe-plugin-query="app_id=419052808285249&amp;container_width=1887&amp;href=https%3A%2F%2Fwww.ficoumaisfacil.com.br%2Flazer%2Farquivos%2Fprojcalc%2Fcalcproj.htm&amp;locale=pt_BR&amp;sdk=joey&amp;share=true&amp;show_faces=true&amp;width=450"><span style="vertical-align: bottom; width: 450px; height: 20px;"><iframe name="f29afe4eaeb473" width="450px" height="1000px" data-testid="fb:like Facebook Social Plugin" title="fb:like Facebook Social Plugin" frameborder="0" allowtransparency="true" allowfullscreen="true" scrolling="no" allow="encrypted-media" src="https://www.facebook.com/v2.5/plugins/like.php?app_id=419052808285249&amp;channel=https%3A%2F%2Fstaticxx.facebook.com%2Fx%2Fconnect%2Fxd_arbiter%2F%3Fversion%3D46%23cb%3Df2623ae07508818%26domain%3Dwww.ficoumaisfacil.com.br%26is_canvas%3Dfalse%26origin%3Dhttps%253A%252F%252Fwww.ficoumaisfacil.com.br%252Ff1af2ffe4cf4d78%26relation%3Dparent.parent&amp;container_width=1887&amp;href=https%3A%2F%2Fwww.ficoumaisfacil.com.br%2Flazer%2Farquivos%2Fprojcalc%2Fcalcproj.htm&amp;locale=pt_BR&amp;sdk=joey&amp;share=true&amp;show_faces=true&amp;width=450" style="border: none; visibility: visible; width: 450px; height: 20px;" class=""></iframe></span></div>
<div class="fb-follow" data-href="http://www.facebook.com/ficoumaisfacil"></div>
<hr>
<div><a href="#" onclick="history.back()"><img src="../../../imagens/backbutton.gif"></a>&nbsp;
&nbsp;
<a href="../../../index.php"><img title="Portal Ficou Mais Fácil" alt="Portal Ficou Mais Fácil" src="../../../imagens/homebutton.gif"></a>&nbsp;
&nbsp;
<a href="mailto:faleconosco@ficoumaisfacil.com.br"><img alt="Fale conosco" title="Fale conosco" src="../../../imagens/mailbutton.gif"></a></div>
</center>
<iframe name="oauth2relay905523654" id="oauth2relay905523654" src="https://accounts.google.com/o/oauth2/postmessageRelay?parent=https%3A%2F%2Fwww.ficoumaisfacil.com.br&amp;jsh=m%3B%2F_%2Fscs%2Fabc-static%2F_%2Fjs%2Fk%3Dgapi.lb.pt_BR.6bdaKiuQqKA.O%2Fd%3D1%2Frs%3DAHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw%2Fm%3D__features__#rpctoken=664223038&amp;forcesecure=1" tabindex="-1" aria-hidden="true" style="width: 1px; height: 1px; position: absolute; top: -100px;"></iframe><div id="volume-booster-visusalizer">
                    <div class="sound">
                        <div class="sound-icon"></div>
                        <div class="sound-wave sound-wave_one"></div>
                        <div class="sound-wave sound-wave_two"></div>
                        <div class="sound-wave sound-wave_three"></div>
                    </div>
                    <div class="segments-box">
                        <div data-range="1-20" class="segment"><span></span></div>
                        <div data-range="21-40" class="segment"><span></span></div>
                        <div data-range="41-60" class="segment"><span></span></div>
                        <div data-range="61-80" class="segment"><span></span></div>
                        <div data-range="81-100" class="segment"><span></span></div>
                    </div>
                </div><div style="display: block; visibility: hidden; position: absolute; width: 106px; left: -1000px; top: -1000px;"><table cellpadding="0" cellspacing="0" dir="ltr" style="width:106px;" frame="void" rules="none" class=" gc-bubbleDefault pls-container"><tbody><tr class="gc-reset"><td class="pls-topLeft gc-reset"><img class="gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/border_3.gif"></td><td class="pls-topTail gc-reset"><img class="pls-tailbottom gc-reset" style="width:15px !important; height:9px !important; max-width: 15px !important; max-height: 9px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"><img class="pls-spacerbottom gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td><td class="pls-topRight gc-reset"><img class="gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/border_3.gif"></td></tr><tr class="gc-reset"><td class="pls-vertShimLeft gc-reset"><img class="gc-reset" style="width:1px !important; height:4px !important; max-width: 1px !important; max-height: 4px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td><td class="pls-vertShim gc-reset"><img class="gc-reset" style="width:1px !important; height:4px !important; max-width: 1px !important; max-height: 4px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td><td class="pls-vertShimRight gc-reset"><img class="pls-dropTR gc-reset" style="width:5px !important; height:4px !important; max-width: 5px !important; max-height: 4px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td></tr><tr class="gc-reset"><td class="pls-contentLeft gc-reset"><img class="pls-tailright gc-reset" style="width:9px !important; height:15px !important; max-width: 9px !important; max-height: 15px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"><img class="pls-spacerright gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td><td class="pls-contentWrap gc-reset"><div class="goog-bubble-content gc-reset"><iframe ng-non-bindable="" frameborder="0" hspace="0" marginheight="0" marginwidth="0" scrolling="no" style="margin:0px;position:absolute;z-index:1;border-style:none;outline:none;width:100px;" tabindex="0" vspace="0" width="100%" id="I0_1670280633980" name="I0_1670280633980" src="https://www.youtube.com/subscribe_embed?action_card=1&amp;channelid=UCJ7IWmUQ5VgqPhS6K9lnvWw&amp;usegapi=1&amp;usegapi=1&amp;jsh=m%3B%2F_%2Fscs%2Fabc-static%2F_%2Fjs%2Fk%3Dgapi.lb.pt_BR.6bdaKiuQqKA.O%2Fd%3D1%2Frs%3DAHpOoo-OFScg4C0i4dWbTehnQjW0xgH1Kw%2Fm%3D__features__#id=I0_1670280633980&amp;_gfid=I0_1670280633980&amp;parent=https%3A%2F%2Fwww.ficoumaisfacil.com.br&amp;pfname=&amp;rpctoken=22467319"></iframe></div></td><td class="pls-dropRight gc-reset"><img class="pls-tailleft gc-reset" style="width:12px !important; height:19px !important; max-width: 12px !important; max-height: 19px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"><img class="pls-spacerleft gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td></tr><tr class="gc-reset"><td class="pls-bottomLeft gc-reset"><img class="gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/border_3.gif"></td><td class="gc-reset"><table cellpadding="0" cellspacing="0" style="width:100%" class="gc-reset"><tbody><tr class="gc-reset"><td class="pls-vert gc-reset"><img class="pls-dropBL gc-reset" style="width:4px !important; height:5px !important; max-width: 4px !important; max-height: 5px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td><td class="pls-dropBottom gc-reset"><img class="pls-tailtop gc-reset" style="width:19px !important; height:13px !important; max-width: 19px !important; max-height: 13px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"><img class="pls-spacertop gc-reset" style="width:1px !important; height:1px !important; max-width: 1px !important; max-height: 1px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td></tr></tbody></table></td><td class="pls-vert gc-reset"><img class="pls-dropBR gc-reset" style="width:5px !important; height:5px !important; max-width: 5px !important; max-height: 5px !important;" src="https://ssl.gstatic.com/s2/oz/images/stars/po/bubblev1/spacer.gif"></td></tr></tbody></table></div><div id="fb-root" class=" fb_reset"><div style="position: absolute; top: -10000px; width: 0px; height: 0px;"><div></div></div></div></body></html>
