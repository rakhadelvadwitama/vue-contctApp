<template>
  <Card class="my-2">
    <CardHeader>
      <CardTitle>{{ contact.name }}</CardTitle>
      <CardDescription>{{ contact.phone }}</CardDescription>
    </CardHeader>
    <CardFooter>
      <div class="space-x-2">
        <Button @click="deleteContact(contact.id)">Delete</Button>
        <Button @click="editContact(contact.id)">Edit</Button>
      </div>
    </CardFooter>
  </Card>
</template>

<script setup lang="ts">
import { Button } from './ui/button'
import {
  Card,
  //   CardContent,
  CardDescription,
  CardFooter,
  CardHeader,
  CardTitle
} from '@/components/ui/card'
defineProps(['contact', 'deleteContact', 'editContact'])
</script>
<style scoped></style>
