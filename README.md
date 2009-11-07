mysqlctl
========

mysqlctl is supposed to simplify the manual start/stop/restart

Having installed MySQL 5.1 from source on Max OS X 10.6 Snow Leopard, I don't
have a PrefPane with a nice Acqua button.

I used to start launch it with 

  sudo launchctl load -w /Library/LaunchDaemons/com.mysql.mysqld.plist

but it's a pain. I'd like to

  sudo mysqlctl start


Installation
============

  sudo cp com.mysql.mysqld.plist /Library/LaunchDaemons
  sudo chown root /Library/LaunchDaemons/com.mysql.mysqld.plist
  sudo cp mysqlctl /usr/local/bin
  sudo chmod +x /usr/local/bin/mysqlctl

Make sure that `/usr/local/bin` is in your `PATH`


Credits
=======

I've been greatly inspired by Dan Benjamin's article about [compiling MySQL
on Snow Leopard][danbenjamin]

[danbenjamin]: http://hivelogic.com/articles/compiling-mysql-on-snow-leopard/