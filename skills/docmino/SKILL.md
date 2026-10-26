---
name: docmino
description: Create, edit, organize, publish, and share interactive guides, documents, pages, and projects through the connected Docmino MCP server. Use when the user asks to work with Docmino content.
---

Use the connected Docmino tools for document work. Every action uses the signed-in person's existing Docmino permissions and the scopes they consented to.

Find documents with search and fetch. Use list_workspaces, list_projects, and list_documents to select a workspace. Use get_project and list_project_documents to navigate a project. Return canonical Docmino links with results.

Before creating or rewriting document or page content, call get_authoring_guide for supported MDX, interactive components, and examples. Send raw MDX in content fields and separate metadata in name and summary. Use interactions when they help the requested guide, lesson, calculator, or form.

Before editing an existing document, retrieve get_document and pass its revision as expectedRevision to update_document. Preserve the complete ordered page tree: omitting an existing page deletes it and requires deletion access. For large documents, follow all continuation instructions using the same revision. Never treat partial content as a complete replacement.

On a revision conflict, retrieve the latest snapshot and reconcile the user's intended changes before saving again. Do not retry the old snapshot with a fresh revision. Retrieve the saved document to verify the change and retained pages.

Use open_document when the user wants the rich embedded editor. It has an explicit Save action. If the client cannot render MCP Apps, continue with the document tools or the canonical Docmino link.

Publishing, sharing, moving between audiences, and deletion affect other people or access. Make the target, intended change, and resulting audience clear. Project deletion releases its documents instead of deleting them. Share removal requires sharing access.

Payment processing, new media uploads, internal AI assistance, comments, form responses, billing, and organization membership administration are outside this integration; direct users to https://docmino.com for those workflows. Do not promise an upload flow, charge payments, change organization roles, or substitute document/project shares for organization membership. Preserving existing media or payment components as document content does not provide upload or payment operations.
