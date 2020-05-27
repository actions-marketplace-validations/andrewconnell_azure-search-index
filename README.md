# Azure Cognitive Search Re-indexer

This is a GitHub Action that submits a reindex request to an Azure Cognitive Search resource.

![.github/workflows/test.yml](https://github.com/andrewconnell/azure-search-index/workflows/.github/workflows/test.yml/badge.svg)

## Inputs

This action requires the following inputs:

- **azure-search-instance**: Name of the Azure Cognitive Search resource
- **azure-search-index**: Name of the Azure Cognitive Search index
- **azure-search-admin-key**: Name of the Azure Cognitive Search index *(store this as a [secret](https://help.github.com/en/actions/configuring-and-managing-workflows/creating-and-storing-encrypted-secrets)*)

## Example Usage

```yml
- name: Reindex Azure Cognitive Search index
  uses: andrewconnell/azure-search-index@1.0.0
  with:
    azure-search-instance: my-search-resource-name
    azure-search-index: my-search-index-name
    azure-search-admin-key: ${{ secrets.SEARCH_ADMIN_KEY }}
```