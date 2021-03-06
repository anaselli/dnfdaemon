==========================================
Client API for Python 2.x and 3.x
==========================================

.. automodule:: dnfdaemon

Classes
========

System API
-------------

.. autoclass:: dnfdaemon.DnfDaemonClient
    :members: Lock, Unlock, Exit, SetWatchdogState,GetRepositories, GetRepo, GetConfig, ExpireCache,
    		  GetPackages, GetPackagesByName, GetPackageWithAttributes, GetAttribute, 
    		  GetGroups, GetGroupPackages,Search, SetEnabledRepos, SetConfig, HistorySearch, GetHistoryPackages, 
    		  ClearTransaction, GetTransaction, AddTransaction, Install, Remove, Update, Reinstall, Downgrade, 
    		  BuildTransaction, RunTransaction, ConfirmGPGImport, GroupInstall, GroupRemove
    
Session API
------------

.. autoclass:: dnfdaemon.DnfDaemonReadOnlyClient
    :members: Lock, Unlock, Exit, SetWatchdogState,GetRepositories, GetRepo, GetConfig, ExpireCache,
    		  GetPackages, GetPackagesByName, GetPackageWithAttributes, GetAttribute, 
    		  GetGroups, GetGroupPackages,Search, SetEnabledRepos
    		  
    
Exceptions
============

.. class:: DaemonError(Exception)

Base Exception from the backend

.. class:: AccessDeniedError(DaemonError)

PolicyKit access was denied.

Ex.
User press cancel button in policykit window

.. class:: LockedError(DaemonError)

dnf is locked by another application

Ex.
dnf is running in a another session
You have not called the Lock method to grep the Lock


.. class:: TransactionError(DaemonError)

Error in the dnf transaction.

