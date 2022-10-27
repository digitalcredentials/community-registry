# community-registry
DCC Community issuer registry

A list of known [DIDs](https://www.w3.org/TR/did-core/) that issue [Verifiable Credentials](https://www.w3.org/TR/vc-data-model/) as part of the [Digital Credentials Consortium](https://digitalcredentials.mit.edu) community.  The DIDs in this repository are curated by the DCC.

<b>NOTE:  If you are participating in the JFF Plugfest 2 as a DCC issuing partner, then you are in the right place.  Read on to add your DID...</b>

The purpose of the registry is to identify 'known' DIDs, and thereby enable a verifier to confirm that a given Veriable Credential was signed using a DID from a known issuer.  Without the registry (or something equivalent) all the verifier could tell you was that a credential had been properly signed by a given DID, but not *who* had signed the credentials.  The DID could be under the control of anyone, potentially someone impersonating another individual or organization.

IMPORTANT: The DIDs in this community registry have been curated by the DCC, but only as DIDs known to the DCC for community experimentation. Verifiable Credentials signed with any of the DIDs in this registry should not be ascribed more meaning than that. 

To add your DID to the registry please submit a Pull Request, with your DID added to the [registry.json](registry.json) file.

If you are adding a DID entry that looks like this:

```
"did:key:z6MkpjNqVhDRY55fJ1K8SnRVf9xvkupbbChzxGR3vyukw4Nf":{
      "name":"Best University",
      "location":"Nicest City, Best Province, Greatest Country",
      "url":"https://very.nice.school.ca"
 }
 ```

and the registry file looked like this before adding your DID:

```
{
  "meta":{
    "created":"2022-10-27T17:57:31+00:00",
    "updated":"2022-10-27T17:57:31+00:00"
  },
  "registry":{
    "did:key:z6MkpLDL3RoAoMRTwTgo3rs39ZwssfaPKtGdZw7AGRN7CK4W":{
      "name":"My University",
      "location":"Cambridge, MA, USA",
      "url":"https://digitalcredentials.mit.edu"
    },
    "did:key:z6MkwcvAGvRUZk5TjdAZrBwQdaSYwDTbpEGjCrqR5zWU3Yf3":{
      "name":"My College",
      "location":"Prato, Italy",
      "url":"https://some.domain.org"
    },
    "did:web:credentials.myschool.ca":{
      "name":"My School",
      "location":"Ancaster, ON, Canada",
      "url":"https://some.domain.ca"
    }
  }
}
```

then it should look like this after (note the new entry and the new 'updated' timestamp):

```
{
  "meta":{
    "created":"2022-10-27T17:57:31+00:00",
    "updated":"2022-10-27T18:33:13+00:00"
  },
  "registry":{
    "did:key:z6MkpLDL3RoAoMRTwTgo3rs39ZwssfaPKtGdZw7AGRN7CK4W":{
      "name":"My University",
      "location":"Cambridge, MA, USA",
      "url":"https://digitalcredentials.mit.edu"
    },
    "did:key:z6MkwcvAGvRUZk5TjdAZrBwQdaSYwDTbpEGjCrqR5zWU3Yf3":{
      "name":"My College",
      "location":"Prato, Italy",
      "url":"https://some.domain.org"
    },
    "did:web:credentials.myschool.ca":{
      "name":"My School",
      "location":"Ancaster, ON, Canada",
      "url":"https://some.domain.ca"
    },
    "did:key:z6MkpjNqVhDRY55fJ1K8SnRVf9xvkupbbChzxGR3vyukw4Nf":{
      "name":"Best University",
      "location":"Nicest City, Best Province, Greatest Country",
      "url":"https://very.nice.school.ca"
    }
  }
}
```
