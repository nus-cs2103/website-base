{% set staff = ["Prabhu", "Damith", "Yugin", "Tzer-Bin", "Michael"] %}
{% set tutors = [
  {name: "AW JEAN LENG ADRIAN", nick: "Adrian Aw", nusnet: "e1138459", github: "Chronoxy"},
  {name: "ADRIAN LEONARDO LIANG", nick: "Adrian Liang", nusnet: "e1122248", github: "AgentHagu"},
  {name: "AMBER TAN JUNNING", nick: "Amber", nusnet: "e1157393", github: "ambertan77"},
  {name: "ANANT SHANKER", nick: "Anant", nusnet: "e0959949", github: "Anant1902"},
  {name: "GOEL ARNAV", nick: "Arnav", nusnet: "e1297755", github: "arnav-goel05"},
  {name: "ASHLEY CHANG LE XUAN", nick: "Ashley", nusnet: "e0958221", github: "ashleyclx"},
  {name: "CHONG CHAN HOW", nick: "Chan How", nusnet: "e0969803", github: "ChillinRage"},
  {name: "PRIYADARSHI CHARVI", nick: "Charvi", nusnet: "e1186234", github: "PriyadarshiCharvi"},
  {name: "DARREN TEO HEE HONG", nick: "Darren", nusnet: "e1122143", github: "darHH"},
  {name: "TAN KAH HO DILLON", nick: "Dillon", nusnet: "e0958762", github: "dillontkh"},
  {name: "DOMINIC KOH SONG JUN", nick: "Dominic", nusnet: "e1113750", github: "dominopizzaaaa"},
  {name: "ELINE NGU XIANG EE", nick: "Eline", nusnet: "e1130038", github: "Elinengu"},
  {name: "LOW TSE WEI, ETHAN", nick: "Ethan", nusnet: "e1121930", github: "EthanLoww"},
  {name: "GABRIELLE GIANNA TAN-WININGS", nick: "Gabrielle", nusnet: "e1271786", github: "gabriellegtw"},
  {name: "TAN GUAN QUN", nick: "Guan Qun", nusnet: "e1138392", github: "monobeartae"},
  {name: "NISHIWAKI HIBIKI", nick: "Hibiki", nusnet: "e1430681", github: "h-b-k-nishi"},
  {name: "HUGO CHIA YONG ZHI", nick: "Hugo", nusnet: "e0958868", github: "Hugo-Chia"},
  {name: "ONG KOK YEE ISAAC", nick: "Isaac", nusnet: "e0373113", github: "cocoanautz"},
  {name: "HONG JUNG WOO", nick: "Jay", nusnet: "e0661390", github: "hjungwoo01"},
  {name: "EU JIA XIN", nick: "Jia Xin", nusnet: "e1070593", github: "JiaXinEu"},
  {name: "JOEL GOH MIN FENG", nick: "Joel", nusnet: "e0957940", github: "joelgoh1"},
  {name: "JO AN", nick: "Jon", nusnet: "e1304446", github: "jayjay19630"},
  {name: "KIM JAEHO", nick: "Jose", nusnet: "e0878500", github: "josejhkim"},
  {name: "YONG JUN XI", nick: "Jun Xi", nusnet: "e1130046", github: "TobyCyan"},
  {name: "WANG JUNWU", nick: "Junwu", nusnet: "e1032464", github: "narwhalsilent"},
  {name: "QUAH KAI KIAT", nick: "Kai Kiat", nusnet: "e1121612", github: "kaikquah"},
  {name: "KAILASHWARAN S/O TAMILSELVAM", nick: "Kailash", nusnet: "e0958973", github: "Kailash201"},
  {name: "KELLY BONG JIA QI", nick: "Kelly", nusnet: "e1281087", github: "Bonzzz3"},
  {name: "GARG LAVANYA", nick: "Lavanya", nusnet: "e1249348", github: "lavanyagarg112"},
  {name: "CENSON LEE LEMUEL JOHN ALEJO", nick: "Lemuel", nusnet: "e1122839", github: "Ryuse"},
  {name: "WONG LI YUAN", nick: "Li Yuan", nusnet: "e0985877", github: "lyuanww"},
  {name: "PUTREVU MIHIR NIYOGI", nick: "Mihir", nusnet: "e1122052", github: "mihirniyogi"},
  {name: "LITCHIOWONG NAPASSORN", nick: "Napassorn", nusnet: "e1285886", github: "iamdiluxedbutcooler"},
  {name: "NICHOLAS CHENG DE FEI", nick: "Nicholas Cheng", nusnet: "e1113742", github: "Nicholas-Cheng-De-Fei"},
  {name: "DONG QIANBO", nick: "Qianbo", nusnet: "e1122784", github: "rollingpencil"},
  {name: "RICHIE HSIEH", nick: "Richie", nusnet: "e0957714", github: "richiehx"},
  {name: "RAMU RITHIK VIJAY", nick: "Rithik", nusnet: "e0969886", github: "papataco14"},
  {name: "RYAN CHEN RUI YANG", nick: "Ryan", nusnet: "e1121649", github: "bipplane"},
  {name: "NG WEI HAN, RYAN", nick: "Ryan", nusnet: "e0958919", github: "RyanNgWH"},
  {name: "ANG JING XUAN SELWYN", nick: "Selwyn", nusnet: "e0958415", github: "SelwynAng"},
  {name: "SHAYNE LEONG YU XIANG", nick: "Shayne", nusnet: "e1122545", github: "Shanyey"},
  {name: "HO CHEOK WAI, SHERMAN", nick: "Sherman", nusnet: "e1115290", github: "itsnotsherm"},
  {name: "GUO SIYAN", nick: "Siyan", nusnet: "e1121718", github: "Siyan-G"},
  {name: "CHUA TSE HUI", nick: "Tse Hui", nusnet: "e0970542", github: "cth06-Github"},
  {name: "MAO XIONGKAI", nick: "Xiongkai", nusnet: "e1122410", github: "MAOXIONGKAI"},
  {name: "TAN YI KAI", nick: "Yi Kai", nusnet: "e1406563", github: "kai824"},
  {name: "TAN YIMING", nick: "Yiming", nusnet: "e0970012", github: "tanyyyming"},
  {name: "CHEAH YUE PEI", nick: "Yue Pei", nusnet: "e1130146", github: "JadeCheah"},
  {name: "Lee Yunjeong", nick: "Yunjeong", nusnet: "e0546221", github: "yunjeong-lee"},
  {name: "CHIN ZHEN JIE", nick: "Zhen Jie", nusnet: "e0957597", github: "ChinZJ"},
  {name: "SUE ZHENG LONG", nick: "Zheng Long", nusnet: "e1121671", github: "zhenglong1603"},
  {name: "KONG ZI HUNG", nick: "Zi Hung", nusnet: "e1129887", github: "zihung20"}
]%}

{% set tutorials = [

]%}

{% set students = [

]%}

{% set org_replacements = {

}%}

{% set teams = {

}%}

{% set products = {

}%}

{% set users = {

}%}

{% set values = {

}%}

{# format: [team, reviewer, reviewee1, backup1, reviewee2, backup2]
From the same tutorial. One for coding standard review, one for code quality.
 #}

{% set ip_pr_review_allocation = [

]%}

{% set ip_pr_slap_review_allocation = [

]%}

{% set tp_dg_review_allocation = [

] %}

{% set team_review_allocation = [

] %}
