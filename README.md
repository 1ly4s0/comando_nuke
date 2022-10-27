![Node build](https://github.com/eritislami/evobot/actions/workflows/node.yml/badge.svg)

![logo](https://cdn.discordapp.com/attachments/933698201486237716/947555143795228682/Diseno_sin_titulo_22.png)

# 🤖 Tutorial Discord Bot (TECNO BROS)
> Código del bot del tutorial de TECNO BROS, el vídeo es [este](https://youtu.be/5Rn375Uzh4c)
## Requisitos

1. Tener un bot de Discord creado **[Guía](https://www.youtube.com/watch?v=qXev2kf-q_0)**
2. Tener Discord.js V12 o Discord.js V13 **[Guía](https://www.youtube.com/watch?v=qXev2kf-q_0)**
3. Tener el bot hosteado o en tu PC **[Guía](https://www.youtube.com/watch?v=0MkVTtLoMiI)**  
4.1 **(Opcional)** Tener el bot en algun host **[Guía](https://www.youtube.com/watch?v=0MkVTtLoMiI)**

## 🚀 Código de NUKE

```js
const Discord = require("discord.js");
const { MessageEmbed } = require("discord.js");

const db = require("quick.db");

const client = new Discord.Client({
    intents: 3276799
});

client.on("messageCreate", async message => {
    if(message.content.startsWith("tb!nuke")) {
        if(!message.member.permissions.has("MANAGE_CHANNELS")) return message.reply("No tienes permisos para usar este comando.")

        message.channel.clone().then(channel => {
            channel.setPosition(message.channel.position)
            const Embed = new Discord.MessageEmbed()
            .setTitle("Canal Nukeado")
            .setDescription(`El canal ${message.channel.name} ha sido nukeado por ${message.author.tag}`)
            .setImage("https://media.tenor.com/Y5FIRkOAIe8AAAAd/shaktii-nuclear-missile-at-the-indian-armys-pokhran-test-range-in-rajasthan-gif.gif")

            message.channel.delete()
            channel.send({ embeds: [Embed] });
        })
    }
})

```
Después de modificar o añadir algo al código, recuerda o reiniciar tu bot o usar el comando `node index.js` para que los cambios se apliquen.

## ⚙️ Uso:

## NUKE
![logo](https://cdn.discordapp.com/attachments/933698201486237716/1035169457326268416/unknown.png)




## 📝 Créditos
* [DISCORD](https://discord.gg/tecnobros)
* [YOUTUBE](https://youtube.com/tecnobros)

Copyright © **1ly4s0#2477** - 2022
