====== Официальные файлы README для Slackware ======

Знаете ли вы, что отличный источник информации о Slackware находится прямо на DVD-диске (или на FTP-сервере)?

Многие люди понимают лишь позже (иногда спустя годы после начала работы со Slackware), что в корне дерева дистрибутива находится несколько текстовых файлов, содержащих информацию о дистрибутиве, структуре содержимого DVD-диска и инструкции по установке и настройке программного обеспечения. Очень жаль, ведь они содержат бесценную информацию для настройки системы Slackware.

Давайте начнем со списка этих файлов в том виде, в каком они представлены на DVD-диске Slackware 15.0:
<code>
ANNOUNCE.15.0
CHANGES_AND_HINTS.TXT
CHECKSUMS.md5
CHECKSUMS.md5.asc
COPYING
COPYING3
COPYRIGHT.TXT
CRYPTO_NOTICE.TXT
ChangeLog.txt
FILELIST.TXT
GPG-KEY
PACKAGES.TXT
README.TXT
README.initrd
README_CRYPT.TXT
README_LVM.TXT
README_RAID.TXT
README_UEFI.TXT
RELEASE_NOTES
SPEAKUP_DOCS.TXT
SPEAK_INSTALL.TXT
Slackware-HOWTO
UPGRADE.TXT
isolinux/README.TXT
source/README.TXT
usb-and-pxe-installers/README_PXE.TXT
usb-and-pxe-installers/README_USB.TXT
</code>

Что содержится в этих файлах?

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/ANNOUNCE.15.0|ANNOUNCE.15.0]]\\ Официальный анонс релиза, описывающий существующие и новые возможности, а также содержащий информацию о приобретении DVD-диска (этот конкретный файл относится к Slackware 14.1).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHANGES_AND_HINTS.TXT|CHANGES_AND_HINTS.TXT]]\\ Список всех новых и удаленных пакетов по сравнению с предыдущим релизом. Также содержит советы и рекомендации по настройке различных компонентов дистрибутива.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHECKSUMS.md5|CHECKSUMS.md5]]\\ Контрольные суммы MD5 для файлов дистрибутива. Чтобы проверить все файлы, используйте эту команду: <code>
tail +13 CHECKSUMS.md5 | md5sum -c --quiet - | less
</code> Каждая строка, в которой нет слова «OK», указывает на поврежденный файл.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CHECKSUMS.md5.asc|CHECKSUMS.md5.asc]]\\ GPG-подпись файла CHECKSUMS.md5 (подписанная [[http://ftp.slackware.com/pub/slackware/slackware-current/GPG-KEY|GPG-ключом проекта Slackware Linux]]). Она позволяет вам убедиться, что значения контрольных сумм в CHECKSUMS.md5 не были изменены злоумышленниками. Следующая команда: <code>
gpg --verify  CHECKSUMS.md5.asc
</code> должна по крайней мере содержать строки, подобные этим двум: <code>
gpg: Signature made Thu 11 Dec 2014 02:46:15 AM CET using DSA key ID 40102233
gpg: Good signature from "Slackware Linux Project <security@slackware.com>"
</code>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYING|COPYING]]\\ Содержит копию лицензии ''GNU GENERAL PUBLIC LICENSE, Version 2, June 1991''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYING3|COPYING3]]\\ Содержит копию лицензии ''GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/COPYRIGHT.TXT|COPYRIGHT.TXT]]\\ Это файл COPYRIGHT для Slackware.  Этот файл предоставляет документацию по многим лицензиям, используемым компонентами, входящими в состав Slackware, а также некоторые благодарности (как обязательные, так и добровольные). Некоторые пакеты будут иметь свой файл лицензии в соответствующем подкаталоге ''/usr/doc''.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/CRYPTO_NOTICE.TXT|CRYPTO_NOTICE.TXT]]\\ Юридическое уведомление в связи с Правилами экспорта США (U.S. Exports Regulations).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/ChangeLog.txt|ChangeLog.txt]]\\ Журнал всех обновлений релиза, сделанных с момента анонса предыдущего выпуска. Своего рода собственный блог Пата :-)

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/FILELIST.TXT|FILELIST.TXT]]\\ Список всех файлов, содержащихся в дереве каталогов для этого релиза.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/GPG-KEY|GPG-KEY]]\\ Публичный ключ, соответствующий закрытому ключу, которым подписаны все пакеты Slackware: <code>
security@slackware.com public key

pub   1024D/40102233 2003-02-26 [expires: 2038-01-19]
uid                  Slackware Linux Project <security@slackware.com>
sub   1024g/4E523569 2003-02-26 [expires: 2038-01-19]
</code>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/PACKAGES.TXT|PACKAGES.TXT]]\\ Подробные сведения о пакетах Slackware, находящихся в каталоге ''./slackware*/'' (описание пакетов, метаданные и список содержимого).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README.TXT|README.TXT]]\\ Файл Slackware README.TXT означает ПРОЧИТАЙТЕ ЭТО В ПЕРВУЮ ОЧЕРЕДЬ!.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README.initrd|README.initrd]]\\ //Slackware initrd mini HOWTO//, описывающее, как создать и установить initrd, который может потребоваться для использования ядра 3.x. Также смотрите "man mkinitrd".

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_CRYPT.TXT|README_CRYPT.TXT]]\\ Руководство HOWTO по установке Slackware на зашифрованные (LUKS-) тома.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_LVM.TXT|README_LVM.TXT]]\\ Руководство HOWTO по установке Slackware на логические тома (LVM).

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/README_RAID.TXT|README_RAID.TXT]]\\ Руководство HOWTO по установке Slackware на корневую файловую систему с программным RAID.

  * [[http://ftp.slackware.com/pub/slackware/slackware64-current/README_UEFI.TXT|README_UEFI.TXT]]\\ Как установить Slackware (при желании сохранив установку Windows нетронутой) на компьютер с UEFI вместо старомодного BIOS. Только для 64-битных ОС.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/RELEASE_NOTES|RELEASE_NOTES]]\\ Этот файл содержит личные заметки Пата о только что завершившемся процессе разработки на пути к стабильному релизу.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/SPEAKUP_DOCS.TXT|SPEAKUP_DOCS.TXT]]\\ Документация для программного обеспечения синтеза речи Speakup.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/SPEAK_INSTALL.TXT|SPEAK_INSTALL.TXT]]\\ Руководство HOWTO по установке с помощью синтеза речи Speakup.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/Slackware-HOWTO|Slackware-HOWTO]]\\ Инструкции по установке Slackware с CD/DVD. //Если вы новичок в Slackware, начните с этого//.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/UPGRADE.TXT|UPGRADE.TXT]]\\ Slackware Upgrade HOWTO объясняет, как обновиться с одного стабильного релиза Slackware до следующего.
<note tip>Вы можете использовать ''[[slackware:slackpkg|slackpkg]]'', чтобы в значительной степени автоматизировать этот процесс.</note>

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/isolinux/README.TXT|isolinux/README.TXT]]\\ Как записать загрузочный диск Slackware.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/source/README.TXT|source/README.TXT]]\\ Некоторая информация об исходном коде, использованном для этого релиза Slackware.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/usb-and-pxe-installers/README_PXE.TXT|usb-and-pxe-installers/README_PXE.TXT]]\\ Руководство HOWTO по установке Slackware по сети с использованием загрузки PXE.

  * [[http://ftp.slackware.com/pub/slackware/slackware-current/usb-and-pxe-installers/README_USB.TXT|usb-and-pxe-installers/README_USB.TXT]]\\ Руководство HOWTO по установке Slackware с использованием загрузочной USB-флешки.

Ссылки на вышеуказанные файлы указывают на дерево каталогов «slackware-current» на FTP-сервере. Slackware-current — это разрабатываемый релиз, а значит, ссылки указывают на самую последнюю версию файла. Если же вам нужна версия для конкретного релиза, просто замените слово «'current'» в URL-адресе на версию релиза, например «''13.37''» или «''14.1''». Эти файлы идентичны для 32-битной и 64-битной версий Slackware.

====== Источники ======
  * Автор оригинальной статьи: [[wiki:user:alienbob|Eric Hameleers]]
<!-- * Contrbutions by [[wiki:user:yyy | User Y]] -->
  * Перевод [[wiki:user:webmeyer|Dmitri Meyer]]

<!-- Please do not modify anything below, except adding new tags.-->
{{tag>slackware translator_webmeyer}}
