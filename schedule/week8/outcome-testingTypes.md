%%**Unit Testing:**%%

<panel type="danger" header="`W8.7a` Can explain unit testing :star:" expanded no-close>
<include src="../../book/testing/testingTypes/unitTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Identify some unit tests in AddressBook-Level4 (or your own project).

  </panel>
</panel>

<!-- ==================================================================================================== -->

<panel type="info" header="`W8.7b` Can use stubs to isolate an SUT from its dependencies :star::star::star:" expanded no-close>
<include src="../../book/testing/testingTypes/unitTesting/stubs/full.md" />
  <panel header=":dart: Evidence" expanded>

Identify some tests in AddressBook-Level4,
1. that can be made pure unit tests by introducing stubs
2. that are using stubs to isolate the SUT from its dependencies 

  </panel>
</panel>

<!-- ==================================================================================================== -->

<panel type="success" header="`W8.7c` Can explain dependency injection :star::star::star::star:" expanded no-close>
<include src="../../book/testing/dependencyInjection/what/full.md" />
<!-- TODO: add evidence -->
</panel>

<!-- ==================================================================================================== -->

<panel type="success" header="`W8.7d` Can use dependency injection :star::star::star::star:" expanded no-close>
<include src="../../book/testing/dependencyInjection/how/full.md" />
<!-- TODO: add evidence -->
</panel>

<br><!-- ##################################################################################################### -->

%%**Integration Testing:**%%

<panel type="warning" header="`W8.7c` Can explain integration testing :star::star:" expanded no-close>
  <include src="../../book/testing/testingTypes/integrationTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain the difference between unit tests and integration tests. 

  </panel>
</panel>

<!-- ==================================================================================================== -->

<panel type="info" header="`W8.7d` Can do integration testing :star::star::star:" expanded no-close>
  <include src="../../book/testing/testingTypes/integrationTesting/how/full.md" />
  <panel header=":dart: Evidence" expanded>

Use tests from AddressBook-Level4 to illustrate the difference between unit testings and integration testing. Hint: good examples [`seedu.address.storage.StorageManagerTest`](https://github.com/nus-cs2103-AY1718S2/addressbook-level4/blob/master/src/test/java/seedu/address/storage/StorageManagerTest.java),[`seedu.address.logic.commands.AddCommandTest`](https://github.com/nus-cs2103-AY1718S2/addressbook-level4/blob/master/src/test/java/seedu/address/logic/commands/AddCommandTest.java),[`seedu.address.logic.commands.AddCommandIntegrationTest`](https://github.com/nus-cs2103-AY1718S2/addressbook-level4/blob/master/src/test/java/seedu/address/logic/commands/AddCommandIntegrationTest.java)

  </panel>
</panel>

<br><!-- ##################################################################################################### -->

%%**System Testing:**%%

<panel type="danger" header="`W8.7e` Can explain system testing :star:" expanded no-close>
  <include src="../../book/testing/testingTypes/systemTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain what system tests are. Give examples from your own project.

  </panel>
</panel>

<!-- ==================================================================================================== -->

<panel type="info" header="`W8.7f` Can explain automated GUI testing :star::star::star:" expanded no-close>
  <include src="../../book/testing/testAutomation/testingGuis/full.md" />
  <panel header=":dart: Evidence" expanded>

Why is automated testing of GUIs is hard? What can we do about it?

  </panel>
</panel>

<br><!-- ##################################################################################################### -->

%%**Acceptance Testing:**%%

<panel type="warning" header="`W8.7g` Can explain acceptance testing :star::star:" expanded no-close>
  <include src="../../book/testing/testingTypes/acceptanceTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain what acceptance tests are. Explain how acceptance testing of your project will be done. 

  </panel>
</panel>

<br><!-- ==================================================================================================== -->

<panel type="info" header="`W8.7h` Can explain the differences between system testing and acceptance testing :star::star::star:" expanded no-close>
  <include src="../../book/testing/testingTypes/acceptanceTesting/acceptanceVsSystemTesting/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain the difference between system tests and acceptance tests. Explain why both are needed.

  </panel>
</panel><p/>


<br><!-- ##################################################################################################### -->

%%**Alpha/Beta Testing:**%%

<panel type="info" header="`W8.7i` Can explain alpha and beta testing :star::star::star:" expanded no-close>
  <include src="../../book/testing/testingTypes/alphaBetaTesting/what/full.md" />
  <panel header=":dart: Evidence" expanded>

Explain alpha and beta testing. How can you do alpha and beta testing in your project?

  </panel>
</panel>
