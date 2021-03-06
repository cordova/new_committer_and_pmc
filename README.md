# Apache Cordova New Committer and PMC Member Process


<a href="https://github.com/apache/cordova-new-committer-and-pmc/issues/new" class="btn btn-primary float-right" role="button" data-hotkey="c">
**File a new issue for the checklist.**</a>

Don't use real names since an invitation can be rejected or the Apache Board can veto PMC inclusion.

## Description
---

So, you've decided to invite a community member to be a committer and Project Management Committee (PMC) member, what do you do?

## 1. Send a [VOTE] thread to private@

See https://community.apache.org/newcommitter.html#committer-vote-template and https://community.apache.org/newcommitter.html#pmc-vote-template

However, we vote on a community member to be **a Committer AND a PMC member** at the same time, so the subject and intro line of the email should reflect as such.



```
Subject: [VOTE] Nominating New Committer and PMC Member: XXXX

Hey everyone,

I would like to nominate XXXX as a Cordova committer and PMC member.
[JUSTIFICATIONS]

I vote +1
```

## 2. Wait three days (72 hours) or when there is a clear consensus, then close the [VOTE]

Of course there should be some actual votes before closing as well. See https://community.apache.org/newcommitter.html#close-vote

## 3. Send an Invite email to the community member, cc private@

Use the template below. Note the words **"PMC membership is subject
to approval by the ASF Board."**, this allows you to send the Board PMC notice straight away. If the board objects, they can still be a committer.

```
Subject: Invitation to become an Apache Cordova committer & PMC member: XXXXXX

Hello XXXXXX!
 
The Apache Cordova Project Management Committee (PMC) hereby offers
you committer privileges to the project, as well as membership in the
PMC. These privileges are offered on the understanding that you'll use
them reasonably and with common sense. We like to work on trust rather
than unnecessary constraints.

Being a committer enables you to more easily make changes without
needing to go through the patch submission process. Being a PMC member
enables you to guide the direction of the project. PMC membership is subject
to approval by the ASF Board.

Being a committer does not require you to participate any more than
you already do.

Of course, you can decline and instead remain as a contributor,
participating as you do now.

A. This personal invitation is a chance for you to accept or decline
in private.  Either way, please let us know in reply to the
private@cordova.apache.org address only.

B. If you accept the invitation, you will also have to choose a unique
Apache account username and let us know. We need this before we can
proceed with account creation and assigning required permissions. To
verify that your desired username does not already exist, please head
over to the people index [1] and do a quick search to see if the login
id is in use. Please also choose an email forwarding address for your
Apache account.

NOTE: You will also need to submit an iCLA [2] in order to accept this invitation.

Thanks for your prompt response,
The Apache Cordova Project Management Committee

[1] https://people.apache.org/committer-index.html
[2] https://www.apache.org/licenses/icla.pdf

Regards,

The Apache Cordova Project Management Committee
```

## 4. Send a PMC Notice to board@apache, and cc private@cordova..

Use the template below. 

```
[NOTICE] XXXX for Cordova PMC

Apache Cordova proposes to invite XXXX to join the PMC.

Vote link:  
(NOTE: use a permalink to the vote result from the procedure below)
```

For the **vote result link**, 
[login first](https://lists.apache.org/oauth.html), then go [here](https://lists.apache.org/list.html?private@cordova.apache.org) to see the private@ archive. Find the vote result email and copy the permalink.

## 5. When the new committer accepts the invite, create a new account for the user (PMC Chair only)

Create [a new account](https://whimsy.apache.org/officers/acreq) (make sure the user has sent an iCLA, if not you can't create a new account).

If the user **already has an Apache account** (due to being a committer from another Apache project), you would just add them to the project as a committer through: 

**Automatically:**
Use [Whimsy](https://whimsy.apache.org/roster/committee/cordova):
1. Press the `Add` button
2. Search for their Apache Id
3. Check the `72 hour board@ NOTICE period elapsed?` checkbox
4. Select the `Add as committer` button

or **[manually](https://www.apache.org/dev/pmc.html#SVNaccess)**.

## 6. Once 72 hours has elapsed from the board@ notice, add the committer to the PMC committee-info.txt file and LDAP (PMC Chair only)

**Automatically:**
Use [Whimsy](https://whimsy.apache.org/roster/committee/cordova):
1. Press the `Add` button
2. Search for their Apache Id
3. Check the `72 hour board@ NOTICE period elapsed?` checkbox
4. Select the `Add to PMC` button

**Manually:**
1. (committee-info.txt - any PMC member has write access) Update https://svn.apache.org/repos/private/committers/board/committee-info.txt with the new PMC member's details and the effective join date **(date that the file was updated)**. **Spaces**, not tabs!
2. (LDAP) If that fails, you will need to SSH to `minotaur.apache.org` and run the `modify_committee.pl` command (run it without parameters to see the help text). Login to minotaur.a.o is only through public key SSH.

## 7. Automatically subscribe the new PMC member to the private list

For example to add name@example.com to the private@cordova.apache.org mailing list, email to:
```
private-subscribe-name=example.com@cordova.apache.org
```
Use this [CodePen](https://codepen.io/shazron/pen/yXVbXr) to encode it.

## 8. Add the PMC member to the JIRA 'PMC' User Role

1. Go to the [Cordova JIRA Project Settings](https://issues.apache.org/jira/plugins/servlet/project-config/CB/summary)
2. Go to `Users and Roles`
3. Select `Add Users to a Role`
4. Search for the user, and add to the `PMC` role

## 9. Ask the PMC member to link their GitHub account

Go to [Gitbox](https://gitbox.apache.org/setup/)

## 10. Invite the PMC member to the `#pmc` Slack Channel

If the new PMC member is using Slack, invite them to the private `#pmc` Slack channel
