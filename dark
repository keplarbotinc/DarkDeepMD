case 'grupinfo': case 'groupinfo':
try{
 var pic = await ZimBotInc.getProfilePicture(m.chat)
  } catch {
 var pic = 'https://i.ibb.co/Tq7d7TZ/age-hananta-495-photo.png'
  }
let ingfo = `*𝗚𝗥𝗢𝗨𝗣 𝗜𝗡𝗙𝗢*\n\n*𝗡𝗔𝗠𝗘 :* ${groupName}\n*𝗜𝗗 𝗚𝗥𝗢𝗨𝗣:* ${m.chat}\n*𝗠𝗔𝗗𝗘 :* ${moment(`${groupMetadata.creation}` * 1000).tz('Africa/Harare').format('DD/MM/YYYY HH:mm:ss')}\n*𝗚𝗥𝗢𝗨𝗣 𝗢𝗪𝗡𝗘𝗥:* @${groupMetadata.owner.split('@')[0]}\n*𝗔𝗗𝗠𝗜𝗡𝗦 :* ${groupAdmins.length}\n*𝗠𝗘𝗠𝗕𝗘𝗥𝗦 :* ${participants.length}\n*𝗗𝗘𝗦𝗖 :* \n${groupMetadata.desc}`
ds = await getBuffer(pic)
ZimBotInc.sendMessage(m.chat, { image: ds,caption: ingfo, mentions: [groupMetadata.owner] }, { quoted: m})
break
 case 'tagall': case 'tag': {
   if (!m.isGroup) throw mess.group
   if (!isBotAdmins) throw mess.botAdmin
   if (!isAdmins) throw mess.admin
let teks = ` 
 ┏━━━━━━━━━━━┑
 ┃🌟𝗧𝗔𝗚𝗔𝗟𝗟🌟
 ┃┄┄┄┄┄┄┄┄┄┄┄┊
 ┃*𝐌𝐄𝐒𝐒𝐀𝐆𝐄 : ${q ? q : '🦇'}*\n\n
 ┗━━━━━━━━ 
`
 for (let mem of participants) {
   teks += `┃⬤ @${mem.id.split('@')[0]}\n`
   }
   ZimBotInc.sendMessage(m.chat, { text: teks, mentions: participants.map(a => a.id) }, { quoted: m })
   }
   break
   case 'hidetag': {
 if (!m.isGroup) throw mess.group
 if (!isAdmins) throw mess.admin
 ZimBotInc.sendMessage(m.chat, { text : q ? q : '' , mentions: participants.map(a => a.id)}, { quoted: m })
 }
 break
