## API Report File for "@backstage/plugin-techdocs"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="react" />

import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { Config } from '@backstage/config';
import { CSSProperties } from '@material-ui/styles';
import { DiscoveryApi } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { EntityName } from '@backstage/catalog-model';
import { IdentityApi } from '@backstage/core-plugin-api';
import { Location as Location_2 } from '@backstage/catalog-model';
import { RouteRef } from '@backstage/core-plugin-api';

// @public (undocumented)
export const DocsCardGrid: ({
  entities,
}: {
  entities: Entity[] | undefined;
}) => JSX.Element | null;

// @public (undocumented)
export const DocsTable: ({
  entities,
  title,
}: {
  entities: Entity[] | undefined;
  title?: string | undefined;
}) => JSX.Element | null;

// @public (undocumented)
export const EmbeddedDocsRouter: (_props: Props) => JSX.Element;

// @public (undocumented)
export const EntityTechdocsContent: (_props: {
  entity?: Entity | undefined;
}) => JSX.Element;

// @public (undocumented)
export type PanelType = 'DocsCardGrid' | 'DocsTable';

// @public (undocumented)
export const Reader: ({ entityId, onReady }: Props_2) => JSX.Element;

// @public (undocumented)
export const Router: () => JSX.Element;

// @public (undocumented)
export type SyncResult = 'cached' | 'updated' | 'timeout';

// @public (undocumented)
export interface TechDocsApi {
  // (undocumented)
  getApiOrigin(): Promise<string>;
  // (undocumented)
  getEntityMetadata(entityId: EntityName): Promise<TechDocsEntityMetadata>;
  // (undocumented)
  getTechDocsMetadata(entityId: EntityName): Promise<TechDocsMetadata>;
}

// @public (undocumented)
export const techdocsApiRef: ApiRef<TechDocsApi>;

// @public
export class TechDocsClient implements TechDocsApi {
  constructor({
    configApi,
    discoveryApi,
    identityApi,
  }: {
    configApi: Config;
    discoveryApi: DiscoveryApi;
    identityApi: IdentityApi;
  });
  // (undocumented)
  configApi: Config;
  // (undocumented)
  discoveryApi: DiscoveryApi;
  // (undocumented)
  getApiOrigin(): Promise<string>;
  getEntityMetadata(entityId: EntityName): Promise<TechDocsEntityMetadata>;
  getTechDocsMetadata(entityId: EntityName): Promise<TechDocsMetadata>;
  // (undocumented)
  identityApi: IdentityApi;
}

// @public (undocumented)
export const TechDocsCustomHome: ({
  tabsConfig,
}: {
  tabsConfig: TabsConfig;
}) => JSX.Element;

// @public (undocumented)
export const TechdocsPage: () => JSX.Element;

// @public (undocumented)
const techdocsPlugin: BackstagePlugin<
  {
    root: RouteRef<undefined>;
    entityContent: RouteRef<undefined>;
  },
  {}
>;
export { techdocsPlugin as plugin };
export { techdocsPlugin };

// @public (undocumented)
export const TechDocsReaderPage: () => JSX.Element;

// @public (undocumented)
export interface TechDocsStorageApi {
  // (undocumented)
  getApiOrigin(): Promise<string>;
  // (undocumented)
  getBaseUrl(
    oldBaseUrl: string,
    entityId: EntityName,
    path: string,
  ): Promise<string>;
  // (undocumented)
  getBuilder(): Promise<string>;
  // (undocumented)
  getEntityDocs(entityId: EntityName, path: string): Promise<string>;
  // (undocumented)
  getStorageUrl(): Promise<string>;
  // (undocumented)
  syncEntityDocs(entityId: EntityName): Promise<SyncResult>;
}

// @public (undocumented)
export const techdocsStorageApiRef: ApiRef<TechDocsStorageApi>;

// @public
export class TechDocsStorageClient implements TechDocsStorageApi {
  constructor({
    configApi,
    discoveryApi,
    identityApi,
  }: {
    configApi: Config;
    discoveryApi: DiscoveryApi;
    identityApi: IdentityApi;
  });
  // (undocumented)
  configApi: Config;
  // (undocumented)
  discoveryApi: DiscoveryApi;
  // (undocumented)
  getApiOrigin(): Promise<string>;
  // (undocumented)
  getBaseUrl(
    oldBaseUrl: string,
    entityId: EntityName,
    path: string,
  ): Promise<string>;
  // (undocumented)
  getBuilder(): Promise<string>;
  getEntityDocs(entityId: EntityName, path: string): Promise<string>;
  // (undocumented)
  getStorageUrl(): Promise<string>;
  // (undocumented)
  identityApi: IdentityApi;
  syncEntityDocs(entityId: EntityName): Promise<SyncResult>;
}

// (No @packageDocumentation comment for this package)
```