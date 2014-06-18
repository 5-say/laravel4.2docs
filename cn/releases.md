# �汾˵��

- [Laravel 4.2](#laravel-4.2)
- [Laravel 4.1](#laravel-4.1)

<a name="laravel-4.2"></a>
## Laravel 4.2

��һ��4.2�汾�İ�װĿ¼�£�ͨ���������php artisan changes������ô˰汾�����ı���б�, Ҳ���Բ鿴Github�ϵı���ļ�(https://github.com/laravel/framework/blob/4.2/src/Illuminate/Foundation/changes.json)�� These notes only cover the major enhancements and changes for the release.

> **ע��:** ��4.2�汾�ķ���������, �ܶ�С��bug�޸��͹��ܸĽ����ϲ�����Laravel 4.1�ĸ��������汾�С� ���ԣ�Ҳһ��Ҫ���Laravel 4.1�ı���б�

### PHP 5.4 Ϊ��Ͱ汾Ҫ��

Laravel 4.2 Ҫ�� PHP 5.4 ����߰汾. ����PHP�汾����������ʹ�������ܹ�ʹ��PHP�������ԣ����磬Ϊ[Laravel Cashier](/docs/billing)�ȹ����ṩ�ĸ��߱������Ľӿڡ� ��PHP 5.3��ȣ�PHP 5.4 ���ٶȺ�ִ��Ч����Ҳ����������ߡ�

### Laravel Forge

Laravel Forge, ��һ���µĲ�����web��Ӧ�ó������ṩһ�ּ򵥵ķ�ʽ�������͹������Լ��ƶ˵�PHP������Щ�������Linode�� DigitalOcean�� Rackspace���� Amazon EC2�� ֧���Զ�������Nginx�� ����SSH key, Cron job �Զ���, ͨ�� NewRelic �� Papertrail���еķ�����, "Push To Deploy", ����Laravel���й���, ����, Forge�ṩ�������õķ�ʽ�������������LaravelӦ�ó���

Ĭ������£�Laravel 4.2��װĿ¼�µ��ļ�`app/config/database.php`����������Forge��, ʹ���µ�Ӧ���ܸ�����Ĳ������ƽ̨������

��Forge�Ĺٷ���վ(https://forge.laravel.com)�ϣ������ҵ�����Ĺ���Laravel Forge����Ϣ��

### Laravel Homestead

Laravel Homestead��һ���ٷ���Vagrant������������������ǿ����Laravel��PHPӦ�ó��������ӱ�����ɷ�֮ǰ�����ӹ�Ӧ����ľ��󲿷ֻᱻ�����������Ӽ�����ٵ������� Homestead����Nginx 1.6��PHP 5.5.12��MySQL��Postgres��Redis��Memcached��Beanstalk��Node��Gulp��Grunt��Bower��Homestaed����һ���򵥵������ļ���Homestead.yaml���������ڵ��������������LaravelӦ�ó���.

���ڣ�Ĭ�ϵ�Laravel 4.2��װĿ¼����һ�������ļ���app/config/local/database.php����������������ʹ�����������Homestead���ݿ��, ��ʹ��Laravel��ʼ����װĿ¼�����ø��ӷ���.

�ٷ��ĵ��Ѿ�����Homestead�ĵ�(/docs/homestead)��

### Laravel ����

Laravel ������һ���򵥵ġ����ڱ������Ŀ⣬��������������Ķ��ļƷѡ�����Laravel 4.2�����룬���ܰ�װ���������Ȼ�ǿ�ѡ�ģ�����������Laravel���ĵ��������Cashier�ĵ��� ����汾��Cashier�޸��˺ܶ�bug, ֧�ֶ����, ���������µ�����API��

### �ػ����̶��й���

Artisan�ġ�queue:work����������֧�֡�--daemon��ѡ�����������һ�����ػ�����ģʽ���Ĺ��ˣ� ���ģʽʹ�ù����ڲ���Ҫ������ܵ�����¼��������� ��������ļ���CPU��ʹ���ʣ������ֻ��ʹ��Ӧ�ó���Ĳ���������Ը��ӡ�

�ڶ����ĵ���/docs/queue#daemon-queue-workers�������ҵ�����Ķ��й�����ص���Ϣ��

### �ʼ��ӿ���������

Laravel 4.2Ϊ���ʼ��������������µ�Mailgun��Mandrill�ӿ��������򡣶Ժܶ�Ӧ�ó�����˵������SMTP��ʽ���˽ӿ��ṩ��һ�ָ���͸��ɿ����͵����ʼ��ķ������µ������������Guzzle 4 HTTP�⡣

### ��ɾ������

һ��Ϊ����ɾ������������ȫ�ַ�Χ�������ĸ��ɾ��ļܹ�ͨ��PHP 5.4�����Ա���������������¼ܹ����ǵ��˸��򵥵Ĺ���ȫ�����Եȹ��ܣ� ��һ�����ɾ��Ŀ�ܱ���Ĺ�ע����롣

���ĵ���/docs/eloquent#soft-deleting�������ҵ�����Ĺ��ڡ���ɾ�����ԡ�����Ϣ��

### �������֤ �� ��������

The default Laravel 4.2 installation now uses simple traits for including the needed properties for the authentication and password reminder user interfaces. This provides a much cleaner default `User` model file out of the box.

### "Simple Paginate"

A new `simplePaginate` method was added to the query and Eloquent builder which allows for more efficient queries when using simple "Next" and "Previous" links in your pagination view.

### Migration Confirmation

In production, destructive migration operations will now ask for confirmation. Commands may be forced to run without any prompts using the `--force` command.

<a name="laravel-4.1"></a>
## Laravel 4.1

### ȫ������б�

The full change list for this release by running the `php artisan changes` command from a 4.1 installation, or by [viewing the change file on Github](https://github.com/laravel/framework/blob/4.1/src/Illuminate/Foundation/changes.json). These notes only cover the major enhancements and changes for the release.

### New SSH Component

An entirely new `SSH` component has been introduced with this release. This feature allows you to easily SSH into remote servers and run commands. To learn more, consult the [SSH component documentation](/docs/ssh).

The new `php artisan tail` command utilizes the new SSH component. For more information, consult the `tail` [command documentation](http://laravel.com/docs/ssh#tailing-remote-logs).

### Boris In Tinker

The `php artisan tinker` command now utilizes the [Boris REPL](https://github.com/d11wtq/boris) if your system supports it. The `readline` and `pcntl` PHP extensions must be installed to use this feature. If you do not have these extensions, the shell from 4.0 will be used.

### Eloquent Improvements

A new `hasManyThrough` relationship has been added to Eloquent. To learn how to use it, consult the [Eloquent documentation](/docs/eloquent#has-many-through).

A new `whereHas` method has also been introduced to allow [retrieving models based on relationship constraints](/docs/eloquent#querying-relations).

### Database Read / Write Connections

Automatic handling of separate read / write connections is now available throughout the database layer, including the query builder and Eloquent. For more information, consult [the documentation](/docs/database#read-write-connections).

### Queue Priority

Queue priorities are now supported by passing a comma-delimited list to the `queue:listen` command.

### Failed Queue Job Handling

The queue facilities now include automatic handling of failed jobs when using the new `--tries` switch on `queue:listen`. More information on handling failed jobs can be found in the [queue documentation](/docs/queues#failed-jobs).

### Cache Tags

Cache "sections" have been superseded by "tags". Cache tags allow you to assign multiple "tags" to a cache item, and flush all items assigned to a single tag. More information on using cache tags may be found in the [cache documentation](/docs/cache#cache-tags).

### Flexible Password Reminders

The password reminder engine has been changed to provide greater developer flexibility when validating passwords, flashing status messages to the session, etc. For more information on using the enhanced password reminder engine, [consult the documentation](/docs/security#password-reminders-and-reset).

### Improved Routing Engine

Laravel 4.1 features a totally re-written routing layer. The API is the same; however, registering routes is a full 100% faster compared to 4.0. The entire engine has been greatly simplified, and the dependency on Symfony Routing has been minimized to the compiling of route expressions.

### Improved Session Engine

With this release, we're also introducing an entirely new session engine. Similar to the routing improvements, the new session layer is leaner and faster. We are no longer using Symfony's (and therefore PHP's) session handling facilities, and are using a custom solution that is simpler and easier to maintain.

### Doctrine DBAL

If you are using the `renameColumn` function in your migrations, you will need to add the `doctrine/dbal` dependency to your `composer.json` file. This package is no longer included in Laravel by default.