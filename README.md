# Materials Cloud Badge

A selection of available badges from this repository:

**Sections**:

[![Materials Cloud Learn section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_learn.svg)](https://materialscloud.org/learn/)  
[![Materials Cloud Work section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_work.svg)](https://materialscloud.org/work/)  
[![Materials Cloud Discover section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_discover.svg)](https://materialscloud.org/discover/)  
[![Materials Cloud Explore section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_explore.svg)](https://materialscloud.org/explore/)  
[![Materials Cloud Archive section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_archive.svg)](https://archive.materialscloud.org)

**Sub-sections**:

[![Materials Cloud Tools](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_tools.svg)](https://materialscloud.org/tools/)  
[![Materials Cloud AiiDAlab](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_aiidalab.svg)](https://materialscloud.org/aiidalab/)

## Usage

You can copy-paste the following code snippets into your document, depending on the relevant language used.

**MarkDown**:

Exchange `SECTION` with the relevant section or sub-section you wish to point to.
See [the section below](#available-sections) for a list of available `SECTION`s.

```markdown
[![Materials Cloud SECTION](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_SECTION.svg)](https://materialscloud.org/SECTION/)
```

### Available `SECTION`s

| `SECTION` | Resulting badge |
|:---:|:---:|
| learn | [![Materials Cloud Learn section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_learn.svg)](https://materialscloud.org/learn/)   |
| work | [![Materials Cloud Work section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_work.svg)](https://materialscloud.org/work/) |
| discover | [![Materials Cloud Discover section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_discover.svg)](https://materialscloud.org/discover/) |
| explore | [![Materials Cloud Explore section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_explore.svg)](https://materialscloud.org/explore/) |
| archive | [![Materials Cloud Archive section](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_archive.svg)](https://archive.materialscloud.org) |
| tools | [![Materials Cloud Tools](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_tools.svg)](https://materialscloud.org/tools/) |
| aiidalab | [![Materials Cloud AiiDAlab](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_aiidalab.svg)](https://materialscloud.org/aiidalab/) |

### Point to a tool hosted on MaterialsCloud

To point to a specific tool hosted on MaterialsCloud you _need_ to know the direct URL to your tool or at the very least the URI name used for the tool (e.g., `qeinputgenerator` for the Quantum ESPRESSO Input Generator tool).  
Exchange `TOOL-NAME` in the following examples with the tool's URI name as explained above.

Example: [![Materials Cloud Tool qeinputgenerator](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_tools.svg)](https://materialscloud.org/work/tools/qeinputgenerator)

**MarkDown**:

```markdown
[![Materials Cloud Tool TOOL-NAME](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_tools.svg)](https://materialscloud.org/work/tools/TOOL-NAME)
```

### Point to an discover section hosted on MaterialsCloud

To point to a specific discover section hosted on MaterialsCloud you _need_ to know the direct URL to the section or at the very least the URI name used for the section (e.g., `hcofs-co2` for the discover section "Covalent organic frameworks for carbon capture").  
Exchange `DISCOVER-NAME` with the discover section's URI name as explained above.

Example: [![Materials Cloud Discover hcofs-co2](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_discover.svg)](https://materialscloud.org/discover/hcofs-co2)

**MarkDown**:

```markdown
[![Materials Cloud Discover DISCOVER-NAME](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_discover.svg)](https://materialscloud.org/discover/DISCOVER-NAME)
```

### Point to an explore section hosted on MaterialsCloud

To point to a specific explore section hosted on MaterialsCloud you _need_ to know the direct URL to the section or at the very least the URI name used for the section (e.g., `autowannier` for the explore section from the profile "Automated high-throughput wannierisation").  
Exchange `EXPLORE-NAME` with the explore section's URI name as explained above.

Example: [![Materials Cloud Explore autowannier](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_explore.svg)](https://materialscloud.org/explore/autowannier)

**MarkDown**:

```markdown
[![Materials Cloud Explore EXPLORE-NAME](https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/main/badges/img/mcloud_badge_explore.svg)](https://materialscloud.org/explore/EXPLORE-NAME)
```

## Create new Materials Cloud badges

In order to create new Materials Cloud badges follow these steps:

1. Create a new JSON file under badges/shields_json/ that reflects the new badge.
   As a rule-of-thumb you should only change the `message` value.
2. Create a new branch with the JSON file and push it to [the GitHub repository](https://github.com/materialscloud-org/mcloud-badge).
3. Go to the webpage: https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/materialscloud-org/mcloud-badge/BRANCH/badges/shields_json/mcloud_badge_NEW_BADGE.json.
   Change `BRANCH` and `NEW_BADGE` to the newly created branch name and this part of the new JSON filename, respectively.
4. Copy the page source to a new file under badges/img/ with the same filename as your JSON file, but it should be an SVG file instead.
5. Update the README with the new badge, if necessary (pointing to the SVG file as if it was in the `main` branch instead of the new temporary branch).
6. Finally, commit and push the changes to GitHub, create a PR and squash+merge into `main`, deleting the temporary branch.
