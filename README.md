# "Частично мой Playbook"
     Моя часть Playbook только та, которая касается установки kibana, первые 2/3 написаны не мной и взяты из репозитория с ДЗ.
     Он производит подключение по протоколу SSH к компьютеру с именем localhost (заранее подготовленная, и
настроенная для этого машина), и производит скачивание и установку Elasticsearch и Kibana, а предварительно,
необходимую для их работы версию java. В качестве дополнительных tags я добавил  tag - skip_ansible_lint, для того, чтобы ansible-lint игнорировал некритичные предупреждения.
Playbook сначала собирает необходимые факты о хосте, нужные для установки java, потом
подготавливает папки для скачивания нужных архивов, далее разархивирует архивы в папки прописанные в соответсвующих tasks (в tasks для java то что нужно для java, в tasks для Elasticsearch и Kibana соответственно), и производит установку. Также в tasks прописаны права которые должны быть назначены
соответствующим папкам и файлам.
Исключил из выложенных файлов папку files из-за ее размера.


