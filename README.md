# Deploy Apache2
Paybook recap:
1. Detects the operating system family (Debian or RedHat).
2. Installs Apache2 only on Debian-based systems.
3. Ensures the appropriate web service (apache2 for Debian, httpd for RedHat) is running and enabled on all systems.
4. Verifies the web service is actively running; fails the playbook if not.
5. Updates the default web page (/var/www/html/index.html) with a welcome message on Debian systems only.
6. Checks if two specific URLs return an HTTP 200 status to confirm web server accessibility.

Usage: ansible-playbook -i hosts --ask-pass --ask-become-pass deploy-apache2.yml
Note: Provide the SSH password for both the user and root account.
