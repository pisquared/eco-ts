# Data Structure

App
	systems: array<System>
	instances: array<Instance>

System
	id: string
	name: string
	description: string
	parameters: {id: Parameter}
	relations: {id: Relation}
	initialState: Status

Parameter
	id: string
	name: string
	description: string
	min: number
	max: number

Relation
	id: string
	name: string
	description: string
	domainId: string
	codomainId: string
	type: string
	effect: array<number>

Instance
	systemId: string
	history: array<Status>

Status {parameterId: value}