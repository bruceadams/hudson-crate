# Release notes

- Ensure jobs, plugins and fingerprints directories are owned by the hudson
  user
  These were being set to hudson-owner, which was preventing hudson from
  writing files

- Remove duplicate buildWrappers element from hudson ant job template

- More crate updates for pallet 0.6.3

- Update crates for pallet 0.6.3

- Add script jobs to hudson crate


## pallet-crates-0.5.0


## pallet-crates-0.4.4

- Update for repository management in separate namespaces


## pallet-crates-0.4.3

- Update versions, and add pallet-crates-test dependencies

- Fix hudson tests

- Add :triggers to hudson job configuration

- Unify hudson config file ownership and mode

- Add a build-trigger publisher to the hudson job configuration
  In order to allow specification of child projects, the :build-trigger
  publisher is added, corresponding to the 'Build other projects' option in
  the 'Post-build actions' in the hudson job configuration interface.

  To use this as part of a job configuration add the following:

      :publishers {:build-trigger {:child-projects "ChildProject,
  ChildProject2"}}

- Update hudson with ant task configuration

- Update for 0.5.0-SNAPSHOT
  Change pallet.resource.* to pallet.action.*. Change stevedore calls to
  script functions to use unquote and the pallet.script.lib namespace. 
  Change request to session.  Change build-resources to build-actions.

- Add Ant configuration to Hudson


## pallet-crates-0.4.2

- Add support for svn credentials in hudson job configuration
  In order to access a svn repository with credentials, pass the
  :subversion-credentials keyword to the hudson job definition.  The 
  argument is a map from a name, to a map of :user-name and password


## pallet-crates-0.4.1

- Add :version option to hudson/plugin
  To allow running with a stable version of a plugin, add the :version 
  option to pallet.crate.hudson/plugin.  The jenkins site .../latest/..
  link is not functional at the moment.


## pallet-crates-0.4.0


## pallet-crates-0.4.0-beta-1

- Fix test for jenkins.war name and exclusion of debian from live test

- Extend hudson plugin and job configuration
  pallet.crate.hudson/job now has a :property option for specifying
  properties of plugins for a job. This can also be used with
  :authorization-matrix to specify user permissions for the job.

- Add svn config. Add live test. Use jenkins-ci.org for downloads.

- Update hudson download url

- Added maven crate dependency to hudson crate

- Add greenballs plugin to hudson

- Fix hudson crate when running without security enabled

- working node-list compute service

- Fix file transfers for paths that need shell expansion

- add :aggregator-style-build job option to hudson

- Fix hudson crate to allow cli use when secruty enabled.  closes #15

- Fix hudson ircbot configuration

- Add users, ircbot plugin, to hudson. add gpg crate, update ci server
  defintion

- Started adding user authorisation to hudson

- update hudson config for pre-build merge

- configuration for hudson github plugin

- remove md5 constant from test

- add hudson github plugin

- Update pallets server/ci.  Add some use of hudson-cli to allow triggering
  of builds through pallet.

- remove defresource usage from maven, tomcat and hudson crates

- Updated to use template as a map, and for new Hardware in jclouds nodes

- Refactoring to a more functional implementation

- Made converge run phase by phase, instead of node by node.  Added
  pre-phase. Removed :reload-all from tests to avoid deftype problems.

- Fixed service start-stop configuration, added sed resource, added md5-url
  option, switched to curl

- Various crate changes. Added Changelog

- remote-file with :url option now downloads to a temporary file first, and
  does a mv to the target

- Changed pallet.crate.tomcat/deploy arguments

- changed hudson to pick up tomcat parameters

- Fixes for hudson crate

- Added :version option to hudson/tomcat. Added test-resource-build macro

- Fix hudson/plugin.

- Added target/*all-nodes* and target/*target-nodes*.  Made target vars
  uninitialised. Tidied mock.

- Harmonised do-script, cmd-join, et al.  Added defvar, defn, and println to
  stevedore. minor documentation fixes.

- Added error handling

- Removed deprecation warnings.  Various fixes.

- clean up of crates for new target bindings

- change pallet.target's *target-template* and *target-tag* to *target-node*
  and *target-node-type*

- Added crontab, cruise-control-rb, and nginx crates.  Added a
  tomcat/undeploy. Added a service/init.

- unification of defresource & defcomponent, elimination of atom usage in
  general, formalized sub-phase / execution type

- improvements to pallet ci server config

- Added pallet.admin.username property

- hudson crate has basic functionality

- clojure 1.1 / 1.2 compatibility modifications

- clojure 1.1 / 1.2 compatibility modifications

- Updated tomcat and hudson configuration

- fixed remote-file if statement, pushed *file-transfers* into
  produce-phases, added tests

- added support for blanket security policy grants

- Added tomcat serer.xml. renamed functions in tomcat and hudson in the
  expectation that they are used in a namespace prefixed manner

- fix remote-file :source => :url option keywords

- added local file deployment function and with-restart macro to tomcat crate

- cleanup (option processing)

- Added defnode, lift and configuration phases. Adds declaritive
  configuration definiton.

- added examples directory. fixes towards functional hudson configuration

- added tomcat-user, hudson-plugin and a couple of test fixes

- fixes for tomcat and hudson

- added crates for sphinx, tomcat and hudson. added a service resource.
  tomact and hudson not yet fully functional.  Fixed escaping in
  mysql-script.

