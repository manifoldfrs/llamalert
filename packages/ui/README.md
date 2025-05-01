# LLaMAlert UI Components

Shared UI components for the LLaMAlert project.

## Components
- ConfidenceBar: Visual representation of anomaly detection confidence
- Card: Container component for dashboard elements
- Common styling and themes

## Usage
```tsx
import { ConfidenceBar, Card } from '@llamalert/ui';

function MyComponent() {
  return (
    <Card title="Anomaly Detection">
      <ConfidenceBar score={75} isAnomalous={true} />
    </Card>
  );
}
```