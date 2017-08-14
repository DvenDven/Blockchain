# Blockchain
Блокчейн представляет из себя набор блоков (файлов), в которых записываются и хранятся все переводы средств за всю историю сети. Новые блоки генерируются майнерами в процессе, называемым майнингом. 
Главные преимущества использования блокчейна – это прозрачность проводимых транзакций и множественное копирование всех этих транзакций таким образом, что у каждого участника процесса всегда есть информация о каждом шаге всех партнеров.
Если попробовать описать это попроще – представьте себе большую общую папку на FTP. Вы видите все ее содержимое (никаких скрытых файлов), вы можете быстро посмотреть, кто и в какие подпапки загружал файлы. Какие именно файлы, когда и для кого. 

Но при этом у всех разный доступ к данным файлам. Кто-то может лишь наслаждаться видами и просматривать список файлов в каждой папке. А кто-то (адресат конкретного файла) может скачивать данные себе. Причем никто другой не сможет получить доступ к файлу – только тот, кому он предназначался.

Разные варианты блокчейна используется в разных криптовалютах. Консенсунс  в разных сетях достигается разными алгоритмами.

МЕХАНИЗМ КОНЦЕНСУСА - это набор правил по которым   и будет  синхронизироваться цепь (ВСЕ УЧАСТНИКИ ЦЕПИ, ВСЕ КЛИЕНТЫ)

БЛОК И ТРАНЗАКЦИИ 
 В блоке  хранится результируящая  хэш сумма всех транзакций входящих в этот блок. Этот блок необходим для подтверждения целостности блока 
и того что именно эти транзакции входят  в этот блок. Для вычисления результирующей  хэш-суммы используется дерево Меркла
попарно  хэшируется хэши от транзакций входящих в блок, затем полученные хэши снова попарно хэшируются и так далее до тех пор 
пока не будет получен 1 единственный хэш - единственный хэш называется хэш суммой.

ГЕНЕЗИС БЛОК - это  первый блок  блокчейна в нём есть информация специфичная для этой  цепи 



ЗАПОЛНИТЬ



хэш-функция(ссылка на криптографию в криптовалютах это только термин)
 - это сопоставление одного набора символа 
с другим набором символов 
     Хэш функция - получет на вход набор любых данных, любого объёма 
И сопоставляет  ему уникальный для этого набора входных данных и набор выходных данных фиксированной  длинны. 
Набор входных данных называется прообразом  хэша, набор выходных данных хэшом этих данных(прообраза)
( 0x....... ) НАБОР данных к примеру "война и мир"
	 хэш функция  случайным  образом  зависет от  набора входных данных это означает что невозможно предуагадать какой  именно вид будет 
иметь хэш функция от набора данных. Единственный способ узнать - вычислить  хэш-функцию.
По хэш-функции нельзя определить от каких данных она была получена.
Для каждого набора данных хэш унекален. По хэшу нельзя понять от какого прообраза он был вычаслен.
"для каждого прообраза  существует 1 уникальных хэш". Хэш функция всегда сопоставляет одному прообразу 
Хэш-функция всегда сопоставляет прообраз с его хэшом из одного прообраза всегда получается конкретный уникальный 
для этого прообраза хэш. Даже незначительное именение входных данных приводит к случайным  имененим хэша от
  этих данных невозможно предсказать как изменится хэш если мы изменим входные данные.

хэш от блока
блок содержит в себе некоторые фиксированые значения
к примеру айди  цепи, сложность, также   содерижит время, в  секундах UNIX.
порядковый номер блока, хэш  сумму  транзакций, все транзакции - эти параметры контролируются майнером.
 майнер задаст эти параметры в момент утверждения блока.
блок  должен сообветствовать правилам механизма консенсуса.

ХЭШ ОТ БЛОКА

вычисляется от некоторых переменных блока NONCE
(NONCE)- это произвольное   чисто которое майнер может перебирать чтобы  хэш-функция от блока изменялась. 
Хэш-функция от блока вычисляется по номеру блока, NONCE, времени и не зависит от транзакций, включеных в блок таким образом
майнинг сводится к перебиранию комбинаций  № блока-NONCE-время таким образом чтобы  хэш от этой комбинации сообветствовал
правилам механизма консенсуса данной цепи с данной сложностью, тоесть имел необходимое кол-во
 лидирующих нулей после того как необходмая комбинация будет найдена майнер может включить в блок необработанные транзакции и утвердить блок
 тоесть добавить его в блокчейн.
