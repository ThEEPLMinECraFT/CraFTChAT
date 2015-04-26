#-#*#*#*#*#*#*#*#-#
#-     Nazwa:    -#
#-   CraFTChaT   -#
#-     Autor:    -#
#-ThEEPLMinECraFT-#
#-#*#*#*#*#*#*#*#-#
#
#-#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#-#
# Licencja:                                             #
# - Zakaz podszywania się pod Autora Skryptu!           #
# - Zakaz kopiowania na inne fora, bez mojej zgody!     #
# - Zabraniam zarabiania na moim skrypcie !             #
#-#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#*#-#
#
#-#*#*#*#*#-#
#-   VIP   -#
#-  CHAT   -#
#-#*#*#*#*#-#
#
# VIP:
command /v [<text>]:
        permission: chat.vip
        permission message: &8&l>> &cNie masz uprawnien do tej komendy !
        trigger:
                if arg 1 is set:
                        if player has permission "chat.vip":
                                loop all players:
                                        if loop-player have permission "chat.vip":
                                                broadcast "&8: &6VCHAT &8: : &6&lVIP &8: &7%player%: &b%arg 1%"
# Super VIP:
command /sv [<text>]:
        permission: chat.svip
        permission message: &8&l>> &cNie masz uprawnien do tej komendy !
        trigger:
                if arg 1 is set:
                        if player has permission "chat.vip":
                                loop all players:
                                        if loop-player have permission "chat.vip":
                                                broadcast "&8: &6VCHAT &8: : &b&lS&6&lVIP &8: &7%player%: &b%arg 1%"
#
#-#*#*#*#*#-#
#-  ADMIN  -#
#-  CHAT   -#
#-#*#*#*#*#-#
#
# Admin:
command /a [<text>]:
        permission: chat.admin
        permission message: &8&l>> &cNie masz uprawnien do tej komendy !
        trigger:
                if arg 1 is set:
                        if player has permission "chat.admin":
                                loop all players:
                                        if loop-player have permission "chat.admin":
                                                broadcast "&8: &cACHAT &8: : &c&lADMIN &8: &4%player%: &b%arg 1%"
# MOD:
command /m [<text>]:
        permission: chat.mod
        permission message: &8&l>> &cNie masz uprawnien do tej komendy !
        trigger:
                if arg 1 is set:
                        if player has permission "chat.admin":
                                loop all players:
                                        if loop-player have permission "chat.admin":
                                                broadcast "&8: &cACHAT &8: : &2MOD &8: &a%player%: &b%arg 1%"
# Helper:
command /h [<text>]:
        permission: chat.helper
        permission message: &8&l>> &cNie masz uprawnien do tej komendy !
        trigger:
                if arg 1 is set:
                        if player has permission "chat.admin":
                                loop all players:
                                        if loop-player have permission "chat.admin":
                                                broadcast "&8: &cACHAT &8: : &9HELPER&8: &e%player%: &b%arg 1%"
#
#-#*#*#*#*#*#*#-#
#-  Emotikonki -#
#-#*#*#*#*#*#*#-#
#
command /emotikonki:
	trigger:
		send "            &8&l>>> &cEmotikonki &8&l<<<            "
		send "&8&l>> &c<3  &7- &4❤"
		send "&8&l>> &c=)  &7- &bツ"
		send "&8&l>> &c*+  &7- &c✚"
		send "&8&l>> &c*star  &7- &6✩"
		send "&8&l>> &c*flower  &7- &d✿"
		send "&8&l>> &c*.  &7- &0•"
		send "&8&l>> &c*<>  &7- &a✦"
		send "&8&l>> &c*note  &7- &9♫"
		send "            &8&l>>> &cEmotikonki &8&l<<<            "
on chat:
		replace all "<3" in message with "&4❤&f"
		replace all "=)" in message with "&bツ&f"
		replace all "*+" in message with "&c✚&f"
		replace all "*star" in message with "&6✩&f"
		replace all "*flower" in message with "&d✿&f"
		replace all "*." in message with "&0•&f"
		replace all "*<>" in message with "&a✦&f"
		replace all "*note" in message with "&9♫&f"		
#
#-#*#*#*#*#*#*#-#
#-   Cenzura   -#
#-#*#*#*#*#*#*#-#
#
on chat:
		replace all "kurwa", "chuj" and "chuje" and "debil" and "suka" and "pedal" and "gej" and "jebany" and "suko" and "debil" and "idiota" and "fuck" and "shit" and "ciota" and "kurw" and "pedale" and "kurwy" and "suki" and "dziwki" and "szmata" and "szmaciarz" and "szmaty" and "pierdole" and "japierdole" and "skurwysynie" and "sukinsynie" and "wkurwiony" and "wkurwiasz" and "pierdolony" and "pierdol" and "jeb" and "spierdalaj" and "wypierdalaj" and "huj" and "sukinsynie" and "hwdp" and "jp" with "&1*&2*&3*&4*&5*&6*&7*&8*&9*&f" in the message
#
#-#*#*#*#*#*#*#-#
#-     ANTY    -#
#-   REKLAMA   -#
#-#*#*#*#*#*#*#-#
#
on chat:
		replace all "IP" and "csrv" and "gomc" and "eu" and "net" and "zapraszam na serwer" and "tk" and "pl" and "www" and "serv" and "msvr" and "hostmc" and "https://" and "com" and "fhmc" with "" in the message
#
#-#*#*#*#*#*#*#-#
#-     CHAT    -#
#-#*#*#*#*#*#*#-#
#
command /chat [<text>]:
	permission: chat.chat
	permission message: &8&l>> &cNie masz dostepu do tej koemndy !
	trigger:
		if argument 1 is "off":
			set {chat} to false
			broadcast "&8&l>> &cChat zostal wylaczony przez &7&l%player% &c!"
		if argument 1 is "on":
			set {chat} to true
			broadcast "&8&l>> &cChat zostal wlaczony przez &7&l%player% &c!"
		if argument 1 is "cc":
			broadcast ""
			broadcast " "
			broadcast "  "
      broadcast "   "
			broadcast "    "
			broadcast "     "
			broadcast "      "
			broadcast "       "
			broadcast "        "
			broadcast "         "
			broadcast "          "
			broadcast "           "
			broadcast "            "
			broadcast "             "
			broadcast "              "
			broadcast "               "
			broadcast "                "
			broadcast "                 "
			broadcast "                  "
			broadcast "                   "
			broadcast "                    "
			broadcast "                     "
			broadcast "                      "
			broadcast "                       "
			broadcast ""
			broadcast " "
			broadcast "  "
			broadcast "   "
			broadcast "    "
			broadcast "     "
			broadcast "      "
			broadcast "       "
			broadcast "        "
			broadcast "         "
			broadcast "          "
			broadcast "           "
			broadcast "            "
			broadcast "             "
			broadcast "              "
			broadcast "               "
			broadcast "                "
			broadcast "                 "
			broadcast "                  "
			broadcast "                   "
			broadcast "                    "
			broadcast "                     "
			broadcast "                      "
			broadcast "                       "
			broadcast ""
			broadcast " "
			broadcast "  "
			broadcast "   "
			broadcast "    "
			broadcast "     "
			broadcast "      "
			broadcast "       "
			broadcast "        "
			broadcast "         "
			broadcast "          "
			broadcast "           "
			broadcast "            "
			broadcast "             "
			broadcast "              "
			broadcast "               "
			broadcast "                "
			broadcast "                 "
			broadcast "                  "
			broadcast "                   "
			broadcast "                    "
			broadcast "                     "
			broadcast "                      "
			broadcast "                       "
			broadcast ""
			broadcast " "
			broadcast "  "
			broadcast "   "
			broadcast "    "
			broadcast "     "
			broadcast "      "
			broadcast "       "
			broadcast "        "
			broadcast "         "
			broadcast "          "
			broadcast "           "
			broadcast "            "
			broadcast "             "
			broadcast "              "
			broadcast "               "
			broadcast "                "
			broadcast "                 "
			broadcast "                  "
			broadcast "                   "
			broadcast "                    "
			broadcast "                     "
			broadcast "                      "
			broadcast "                       "
			broadcast ""
			broadcast " "
			broadcast "  "
			broadcast "   "
			broadcast "    "
			broadcast "     "
			broadcast "      "
			broadcast "       "
			broadcast "        "
			broadcast "         "
			broadcast "          "
			broadcast "           "
			broadcast "            "
			broadcast "             "
			broadcast "              "
			broadcast "               "
			broadcast "                "
			broadcast "                 "
			broadcast "                  "
			broadcast "                   "
			broadcast "                    "
			broadcast "                     "
			broadcast "                      "
			broadcast "                       "
			wait a tick
			broadcast "&8&l>> &cChat zostal wyczyszczony przez &7&l%player% &c!"
