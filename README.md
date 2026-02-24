# Nome-trilha_proposito
um app para conectar propósitos e realizar sonhos maravilhosos 
// --- TELA DE MENTORES COM SEUS LINKS ---
class TelaMentores extends StatelessWidget {

  final List<Map<String, String>> profissionais = [

    
    
    
    {
      "nome": "mirian oliveira ",
      "cargo": " mentora de crianças e famílias ",
      "url": "https://linktr.ee/oliveiramiriande"
    
    {
      "nome": "Cida Pacheco",
      "cargo": "Psicanalista e Pro Stility",
      "url": "https://instagran/cidapachecopscanalista"
    },

    {
      "nome": "Cida Pacheco - Grupo",
      "cargo": "Psicanalista e Pro Stility",
      "url": "https://chat.whatsapp.com/GYEBQl9zhnaIEhpxq7sXyV"
    },

    {
      "nome": "Kelly Santos",
      "cargo": "Pastora e Psicanalista",
      "url": "https://chat.whatsapp.com/DFrYTba5JcGBmU8vXpdtS4"
    },

    {
      "nome": "Guilherme Barbosa",
      "cargo": "Engenheiro Civil",
      "url": "https://linkedin.com/in/guilhermebarbosavieira"
    },

    {
      "nome": "Gerson de Oliveira",
      "cargo": "Mestre de Obras",
      "url": "https://share.google/Fs79WdxX9jQo4fvBr"
    },

    {
      "nome": "Grazy Guts",
      "cargo": "Marketing e Vendas",
      "url": "https://instagram.com/grazygutsbrasil"
    },

    {
      "nome": "Tatiana Evangelista",
      "cargo": "Administradora",
      "url": "https://instagram.com/eusoutatianaevangelista"
    },

    {
      "nome": "Assembleia de Oração",
      "cargo": "Missionária",
      "url": "https://wa.me/5531987411630"
    },

    {
      "nome": "Sara Augustini",
      "cargo": "Artesã e Inclusão",
      "url": "https://wa.me/5531983558451"
    },

  ];

  void _abrirLink(String url) async {
    if (await canLaunch(url)) {
      await launch(url);
    }
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("Trilhando com Mentores")),
      body: ListView.builder(
        itemCount: profissionais.length,
        itemBuilder: (context, i) {
          return ListTile(
            leading: CircleAvatar(
              child: Text(profissionais[i]['nome']![0]),
            ),
            title: Text(profissionais[i]['nome']!),
            subtitle: Text(profissionais[i]['cargo']!),
            trailing: Icon(Icons.link),
            onTap: () => _abrirLink(profissionais[i]['url']!),
          );
        },
      ),
    );
  }
}
