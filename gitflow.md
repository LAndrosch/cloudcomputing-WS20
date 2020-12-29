## GitFlow

Using the GitFlow approach it should be made sure that branches are only merged into specific other branches. 

### Branches

#### Develop
The **develop** branch is the main branch vor development.

#### Feature
On **feature** branches one feature is implemented and is then merged back into the *develop* branch.

**Naming scheme**: feature/[name/description-of-the-feature]  
**Branched from**: develop  
**Target**: develop  

#### Release
**Release** branches are used to prepare a new version for the release.

**Naming scheme**: release/[version]  
**Branched from**: develop  
**Target**: 
- master
- develop  

#### Hotfix
**hotfix** branches are used for important fixes in already released versions

**Naming scheme**: hotfix/[description-of-the-fix]  
**Branched from**: master  
**Target**: 
- master
- develop  

