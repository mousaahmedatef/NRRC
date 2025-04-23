                var otherWaitingRepliesExisted = (await repository.FindByCondition(r => r.Id != result.Id && informationEntitiesIds.Contains(r.FkInformationEntityId) && (r.FkStatusId == (int)InformationAndGuidanceReplyStatusEnum.WAITING_REPLY || r.FkStatusId == (int)InformationAndGuidanceReplyStatusEnum.DONE_REPLY))).Any();

