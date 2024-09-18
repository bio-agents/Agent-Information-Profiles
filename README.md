# Agent Information Profiles

A *agent information profile* is a JSON document which specifies which agent attributes - defined in [bioagentsSchema](https://github.com/bio-agents/bioagentsSchema) and also listed in the file [agent_attributes.json](https://github.com/bio-agents/Agent-Information-Profiles/blob/master/agent_attributes.json) - should be specified for different types of agents within a set of agent descriptions.

Within a profile, bioagentsSchema [attributes](https://bioagentsschema.readthedocs.io/en/latest/bioagentsschema_elements.html#) may be specified for different [agent types](https://bioagentsschema.readthedocs.io/en/latest/controlled_vocabularies.html#agent-type) as:  
* **Mandatory** - the attribute **MUST** be defined
* **Recommended** - the attribute **SHOULD** be defined
* **Optional** - the attribute **MAY** be defined
* **Not applicable** - the attribute is not relevant to this agent set and **MUST NOT** be defined.

The key words "MUST", "MUST NOT", "SHOULD", and "MAY", and "OPTIONAL" are to be interpreted as described in [RFC 2119](http://www.ietf.org/rfc/rfc2119.txt):

* "MUST" means that the guideline is an absolute requirement of the specification.
* "MUST NOT" mean that the guideline is an absolute prohibition of the specification.
* "SHOULD" mean that there may exist valid reasons in particular circumstances to ignore a particular guideline, but the full implications must be understood and carefully weighed before doing so.
* "MAY mean that the guideline is truly optional; you can choose to follow it or not.

Agent information profiles **MUST** comply with the Agent Information Profile Schema (a JSON schema), which supports *all* of the bioagentsSchema attributes.

# Example
An information graphic derived from the [IFB Agent Information Profile](https://github.com/bio-agents/Agent-Information-Profiles/blob/master/profiles/ifbAgentInfoProfile.json) is shown below:
<p align="center">
<img src="assets/ifb_info_standard.png" />
</p>



# Application
We anticipate the agent information profiles will be used by a agent description verification service which will provide a sustainable method for reporting on agent description quality within a corpus of agents.

It will take as input 1) a list of bio.agents agent IDs and 2) a agent information profile, and produce as output a report on the compliance of the agent descriptions to the standard, in human and machine-readable formats. Agent descriptions will be consumed in JSON or JSON-LD format, *e.g.* by invoking the [bio.agents](https://bio.agents) API, or from a *bio.agents* data dump.

<p align="center">
<img src="assets/agentDescriptionVerifier.png" />
</p>


# Documentation (for stable version 1.0.0)
Comprehensive documentation is available: 
* [Technical docs](http://bio-agents.github.io/Agent-Information-Profiles/) (built from files under [/stable/docs](https://github.com/bio-agents/Agent-Information-Profiles/tree/master/stable/docs))

# Files

File                            | Description
----                            | -----------
agentInfoProfileSchema_dev.json  | Agent Information Profile Schema - dev version (JSON schema)
stable                          | Current stable version of the schema + docs 
stable/examples                 | Example Agent Information Profiles created using the schema (latest stable version)
docs                            | Technical docs formatted for website (latest stable version).  Hosted [here](http://bio-agents.github.io/Agent-Information-Profiles/) (uses files copied from "stable" folder)
versions                        | Older stable versions of the schema + docs
profiles                        | Agent Information Profiles created thus far
agentAttributesSchema.json       | JSON schema for the agent attributes JSON file
agent_attributes.json	        | Lits of attributes defined in bioagentsSchema in JSON format
agent_attributes_WITH_REGEX.json | Version of agent_attributes.json with regex patterns (ignore for now)
assets                          | Folder for images and other assets
README.md		        | This file






