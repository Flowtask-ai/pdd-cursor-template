# PRD Requests

This folder contains the Product Requirements Documents (PRDs) that you create for your projects.

## Usage

1. Copy a template from `../templates/` based on your use case:
   - `new-bc-XXX.md` - For new bounded contexts
   - `new-feature-YYY-bc-XXX.md` - For new features in existing BCs
   - `improve-bc-XXX.md` - For improving existing BCs

2. Fill in the template with your specific requirements

3. Use the naming convention:
   - `new-bc-<name>.md` (e.g., `new-bc-ecommerce.md`)
   - `new-feature-<feature>-bc-<name>.md` (e.g., `new-feature-auth-bc-user.md`)
   - `improve-bc-<name>.md` (e.g., `improve-bc-payment.md`)

4. Generate a PRP from your PRD using the command: "Generate a PRP from PDD/PRDs/requests/your-file.md"

## Examples

See `../examples/` for filled examples to inspire your PRDs.

## Next Step

Once your PRD is ready, use the PRP generation command and continue the workflow as described in the main README and USAGE_GUIDE.md. 